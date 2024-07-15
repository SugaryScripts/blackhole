up:: [[Home]]
tag:: #map 

# Framework
Comparison:
- [[Pipenv vs virtualenv vs conda]]
- [[comparison pipenv virtualenv conda - Gemini]]

- [[Pyenv]]
- How to use it
	- [[Pipenv]]
	- [[Virtualenv]]
	- Conda
- [[Packages]]
- [[Streamlit]]
- HTTP
	- [[API - python]]
# Command
```sh
python --version
```

> [!NOTE]+ Notes on manjaro user
> Manjaro comes with Python and pip by default. It's **recommended** to install Python packages using **pamac** or **pacman** for better system integration and dependency management. **Except python w/ virtual env** of course.


## pip basic
```sh
pip list | grep $tada
pip list | findstr $tada
pip install/uninstall
```
**Show**/display **list** of packages that installed using pip

## pip freeze
```sh
pip freeze
```
**Generate** list of installed package and their versions as `requirements.txt`. **Excludes** system-wide packages or those not installed by pip.

## Install from requirements
```sh
pip3 install --user -r requirements.txt
```
**--user** : installed on current user only. not system wide
**-r** : install from a file, named requirements.txt


# Tips
### Remove unused dependencies that brought by specific package
```sh
pip install pip-autoremove
pip-autoremove streamlit -y
```
# Troubleshoot
## illegal hardware instruction (core dumped)
Tried:
["zsh: illegal hardware instruction python" when installing Tensorflow on macbook pro M1 - Stack Overflow](https://stackoverflow.com/questions/65383338/zsh-illegal-hardware-instruction-python-when-installing-tensorflow-on-macbook)
[python - How can I properly use Pyenv and venv? - Stack Overflow](https://stackoverflow.com/questions/52731543/how-can-i-properly-use-pyenv-and-venv)
- 3.12.2
- 3.8.5
- 3.7.0
Worked:
- 3.12.3 on windows only