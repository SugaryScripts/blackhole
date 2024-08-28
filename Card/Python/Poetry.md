#### Commands

| Command                                                                                                                     | Description                                                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| `poetry new poetry-demo`                                                                                                    |                                                                                                                                     |
| `poetry install`                                                                                                            |                                                                                                                                     |
| `~ env info` -p                                                                                                             | `-p` for location .venv                                                                                                             |
| poetry config virtualenvs.in-project true                                                                                   | Change .venv to be within project                                                                                                   |
| ~ shell                                                                                                                     |                                                                                                                                     |
| ~ add requests                                                                                                              |                                                                                                                                     |
| ~ remove requests                                                                                                           |                                                                                                                                     |
| ~ env list                                                                                                                  | which environment if active                                                                                                         |
| rm -rf .venv                                                                                                                | uninstall venv (poetry, pipenv)                                                                                                     |
| poetry export -f requirements.txt > requirements.txt                                                                        |                                                                                                                                     |
| `poetry env use 3.7`<br># or<br>`poetry env use /path/to/preferred/python/version<br>`<br>`poetry lock`<br>`poetry install` | Change python ver                                                                                                                   |
| poetry add pendulum@^2.0.5<br>poetry add pendulum@~2.0.5<br>poetry add "pendulum>=2.0.5"<br>poetry add pendulum == 2.0.5    | # Allow >=2.0.5, <3.0.0 <br># Allow >=2.0.5, <2.1.0 <br># Allow >=2.0.5 versions, without upper bound<br># Allow only 2.0.5 version |


#### Pyproject
Use poetry as solely for dependency management