up:: [[Python|Python]]
similar:: [[Pipenv - simplified]] | [[Pipenv vs virtualenv vs conda#Pipenv]]


### Initializing a Project
```
pipenv install
```
This command initializes a new Pipenv project in the current directory. It creates a `Pipfile` and `Pipfile.lock` to manage project dependencies.

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

### Installing Dependencies
```
pipenv install <package_name>
```
This command installs a specific Python package into your project's virtual environment.

**Explanation**:
- `<package_name>` is the name of the package you want to install (e.g., `requests`, `numpy`).
- Pipenv automatically adds the package and its dependencies to the `Pipfile` and updates the `Pipfile.lock` to ensure a reproducible environment.

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

### Activating the Virtual Environment
```
pipenv shell
```
This command activates your project's virtual environment, making the installed packages available for use in your Python scripts.

**Note:** After activating, your shell prompt will typically change to indicate you're in the virtual environment (e.g., `(my_project)user@machine:`).

**Tip:** Deactivate the virtual environment using `exit` when you're finished working on your project.

Result
Creating a new project virtual environment
```sh
/home/$user/.local/share/virtualenvs/$project_name-hashcode
```
Explanation:
- Pipenv creates a virtual environment to isolate project dependencies and avoid conflicts with system-wide packages.
- Activating the environment allows you to use the installed packages within your project.

### Uninstall Pipenv from Project
links:: [[Pipenv - simplified#Uninstall Pipenv from Project|=]]
1. `pipenv --rm`
2. Remove these
- `Pipfile` 
- `Pipfile.lock`

### Uninstall package
- in shell
	```sh
	pipenv uninstall $package
	```
- outside
	
### Commands
- Package
	- install `pipenv install <package_name> ...` 
	  `pipenv install requests==2.27.1`
	- uninstall `pipenv uninstall <package_name> ...`
		- **Default behavior:** By default, Pipenv will remove the uninstalled package and its direct dependencies from the `Pipfile`. This ensures a minimal dependency specification.
		- **`--leave-optional` flag:** You can use the `--leave-optional` flag to instruct Pipenv to keep optional dependencies in the `Pipfile` even if they are no longer required by the remaining installed packages.
		  `pipenv uninstall <package_name> --leave-optional`
