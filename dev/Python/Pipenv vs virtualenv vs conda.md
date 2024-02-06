#literature
[medium@krishnaregmi](https://medium.com/@krishnaregmi/pipenv-vs-virtualenv-vs-conda-environment-3dde3f6869ed)

###### contents
```table-of-contents
style: inlineFirstLevel # TOC style (nestedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
debugInConsole: false # Print debug info in Obsidian console
```


# Virtual Environment
Virtualenv was the default way of creating virtual environment for many years. It is still used by many although people are moving to improved pipenv or conda (explained below).

Here is how you create a new virtual environment. We will talk about why it got replaced by pipenv after that. Pip comes pre-installed for most newer versions (Python 2.7.9+ or 3.4+). But if you don’t have it installed, you can install it by downloading `get-pip.py` file from [https://bootstrap.pypa.io/](https://bootstrap.pypa.io/). Then cd into the downloads directory and run the file as follows:

```sh
cd /path/to/downloadsfolder  
python get-pip.py
```

Once you have pip installed, install virtualenv by running below

```sh
pip install virtualenv
```

Once you have virtualenv installed, you can `cd` into the directory of your choice in the terminal or command prompt, and then run the following:

```sh
virtualenv venv
```

This will create a folder called venv in the directory. You can name your virtualenv folder anything you’d like. To activate run (works in windows only)

```sh
venv\Scripts\activate
```

There you go! thats how you create a new environment. `pip install package` to install any package you need.

To make your repo reusable, make sure to create a record of everything that’s installed in your new environment, run

```sh
pip freeze > requirements.txt
```

If you are creating a new virtual environment from a requirements.txt file, you can run

```sh
pip install -f requirements.txt
```

If you open your requirements file you will see a different package with its version in each line.

As you can see we are creating a virtual environment and then using pip to install packages, and then manually calling `pip freeze` to save whats been installed. What if you didn’t have to make this a two part process? What if you could merge `pip` with `virtualenv` ?

Enter pipenv.

> [[#contents]]

# Pipenv
Pipenv was created due to many shortcomings of virtualenv such as it not making a distinction if project dependency and the dependies of the project dependency, not having mechanism to distinguish dev and production needs etc.

To install pipenv, you need to install pip first. Then do

```sh
pip install pipenv
```

Next, you create a new environment by using

```sh
pipenv install 
```

This will look for a pipenv file, if it doesn’t exist, it will create a new environment and activate it. As you can already see, the workflow is simplified by not seperating the process of creating a new environment from scratch vs creating with a existing file. To activate you can run

```sh
pipenv shell 
```

To install new packages do `pip install package` , and pipenv will automatically add the package to the pipenv file that’s called `Pipfile`. You can also install package for just the dev environement by calling

```sh
pip install <package> --dev
```

> advise anyone to actually use Pipenv instead of virtualenv

[[#contents]]

# Conda
If you are an engineer, or a scientist or use Numpy/Scipy package in windows environment, you have probably experienced the frustration of having to do a lot of work to install numpy/scipy packages. Anaconda is a distribution of python that makes it super simple to install those packages. Anaconda also has their own virtual environment system called conda. Make sure to have Anaconda installed.

To create an environment call this command:

```sh
conda create --name environment_name python=3.6
```

You can save all the info necessary to recreate the environment in a file by calling

```sh
conda env export > environment.yml
```

To recreate the environment you can do the following:

```sh
conda env create -f environment.yml
```

[[#contents]]