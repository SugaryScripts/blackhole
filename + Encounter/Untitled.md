k


# Troubleshoot

# Warning
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
# Command
## Basic
## Package related
