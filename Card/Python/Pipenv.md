up:: [[Python|Python]]
similar:: [[Pipenv vs virtualenv vs conda#Pipenv]]

# How
## Setup pipenv as Manjaro User
Can be achieved without **pip** on system
```sh
sudo pacman -S python python-pipenv
```

# Commands
## Summary
| ref                                        | command                                                 | do                           |
| ------------------------------------------ | ------------------------------------------------------- | ---------------------------- |
| [[#Initializing a Project\|=]]             | `pipenv install`                                        | Init pipenv project          |
| [[#Activating the Virtual Environment\|=]] | `pipenv shell`                                          | Start shell                  |
| [[#Uninstall Pipenv from Project\|=]]      | `pipenv --rm`<br>`rm Pipfile Pipfile.lock`              | Remove pipenv from project   |
|                                            | `pipenv install $package`                               | Install package              |
|                                            | `pipenv uninstall $package`                             | Uninstall package            |
|                                            | `pip list`                                              | List installed package       |
|                                            | `pipenv requirements > requirements.txt`                | Generate requirement.txt     |
|                                            | `pipenv requirements --dev > dev-requirements.txt<br>`  | Optional for dev build       |
|                                            | `pipenv requirements --from-pipfile > requirements.txt` | From pipfile instead of lock |

## Project
### Change .venv to project dir
Set the environment variable
```
export PIPENV_VENV_IN_PROJECT=1
```
.zshrc
windows just
```cmd
set PIPENV_VENV_IN_PROJECT=1
```
### Initializing a Project
```
pipenv install
```
This command initializes a new Pipenv project in the current directory. It creates a `Pipfile` and `Pipfile.lock` to manage project dependencies.

**When to use**:
- When create new project without choosing pipenv
- Project not yet set up with a virtual environment

**Explanation**:
- `pipenv` is the command-line tool for Pipenv.
- `install` tells Pipenv to create a new project and install any initial dependencies listed in the `Pipfile` (if it exists).

**Result**:
(Directory structure)
```
my_project/
  Pipfile
  Pipfile.lock
```

### Activating the Virtual Environment
```
pipenv shell
```
This command activates your project's virtual environment, making the installed packages available for use in your Python scripts.

**Note:** After activating, your shell prompt will typically change to indicate you're in the virtual environment (e.g., `(my_project)user@machine:`).

**Tip:** Deactivate the virtual environment using `exit` when you're finished working on your project.

**Result**:
Creating a new project virtual environment
```sh
/home/$user/.local/share/virtualenvs/$project_name-hashcode
```
Explanation:
- Pipenv creates a virtual environment to isolate project dependencies and avoid conflicts with system-wide packages.
- Activating the environment allows you to use the installed packages within your project.

### Uninstall Pipenv from Project
1. `pipenv --rm`
2. Remove these
- `Pipfile` 
- `Pipfile.lock`

### Pipenv Pyenv
[[Pyenv]]
```sh
pyenv local 3.8.5
pipenv install --python 3.8.5
pipenv --rm
```

## Package
### Installing Dependencies
```
pipenv install <package_name>
```
This command installs a specific Python package into your project's virtual environment.

**Explanation**:
- `<package_name>` is the name of the package you want to install (e.g., `requests`, `numpy`).
- Pipenv automatically adds the package and its dependencies to the `Pipfile` and updates the `Pipfile.lock` to ensure a reproducible environment.
Variant:
install `pipenv install <package_name> ...` 
	  `pipenv install requests==2.27.1`
### Listing Installed Packages on **Pipenv Shell**
```sh
pip list
```
This command displays all the packages currently installed in your project's virtual environment.

Result (Optional):
```
PACKAGE VERSION  DIR LOCATION
requests  2.30.2    /home/user/my_project/venv/lib/python3.9/site-packages
```

### Uninstall package
- in shell
	```sh
	pipenv uninstall $package
	```
- outside
	
### Commands
- Package
	- 
	- uninstall `pipenv uninstall <package_name> ...`
		- **Default behavior:** By default, Pipenv will remove the uninstalled package and its direct dependencies from the `Pipfile`. This ensures a minimal dependency specification.
		- **`--leave-optional` flag:** You can use the `--leave-optional` flag to instruct Pipenv to keep optional dependencies in the `Pipfile` even if they are no longer required by the remaining installed packages.
		  `pipenv uninstall <package_name> --leave-optional`

# Case
##### Change python version
Change python_version on Pipfile.lock then `pipenv install --python=...`
Change it on Pipfile then `pipenv install --python=/path/to/your/python` This would remove the previous virtual environment and create a new one using the python version specified. 

# Troubleshoot

## Warning
## Ignoring invalid distribution ~...
**Trigger**
`pip list` || `pipenv clean`
**Solution**
Please remove those files / folders. By listing them first
```bash
ls -a /xx/xx/xx/lib/pythonx.x/site-packages | grep "^~"
```
Then remove them one by one `rm -R ~...`
**source**
[python - Why do I get this when using pip WARNING: Ignoring invalid distribution -ip? - Stack Overflow](https://stackoverflow.com/questions/68880743/why-do-i-get-this-when-using-pip-warning-ignoring-invalid-distribution-ip)

## Pipenv found itself running within a virtual environment
Courtesy Notice: Pipenv found itself running within a virtual environment, so it will automatically use that environment, instead of creating its own for any project. You can set PIPENV_IGNORE_VIRTUALENVS=1 to force pipenv to ignore that environment and create its own instead. You can set PIPENV_VERBOSITY=-1 to suppress this warning.
**Trigger**
You're Already in a Virtual Environment
**Solution**
Just run `pipenv` outside the shell. Or `exit`  from the pipenv shell first, then run `pipenv ...`

