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
- [[Streamlit]]
# Command
```sh
python --version
```

> [!NOTE]+ Notes on manjaro user
> Manjaro comes with Python and pip by default. It's **recommended** to install Python packages using **pamac** or **pacman** for better system integration and dependency management. **Except python w/ virtual env** of course.


## pip list
```sh
pip list
```
**Show**/display **list** of packages that installed using pip

## pip freeze
```sh
pip freeze
```
**Generate** list of installed package and their versions as `requirements.txt`. **Excludes** system-wide packages or those not installed by pip.




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