up:: [[Home]]
tag:: #map 

# Framework
[[Pipenv vs virtualenv vs conda]]
[[comparison pipenv virtualenv conda - Gemini]]

- How to use it
	- [[Pipenv]]
	- [[Virtualenv]]
	- Conda
- [[Streamlit]]
# Command

```sh
sudo pacman -S python python-pip
```
Install python

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




