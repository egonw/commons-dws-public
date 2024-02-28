---
id: 3xju2sc89n29uayg8f6hega
title: Python and Packages
desc: ''
updated: 1709139680672
created: 1709132173368
---
# Python
To get start with python is very easy. But to come back to a project and let it run again can hurt.
This should be a small introduction how to handle python environements.

## Python versions
As we all, also Python is developping. Some packages are developped for the newest python and a specific time
but not updated for the newest python versions. This can be a problem when you want to use this package, but you just installed the newest version.  

The solution is to use a virtual environment (for example [__conda__](https://anaconda.org/), [__pipenv__](https://pypi.org/project/pipenv/), ect.).  

In this case we will have a look for **pyenv** (the easier way to work with python versions).  

### Pyenv

#### Installation
To install [__pyenv__](https://github.com/pyenv/pyenv) you can use the automatic installer (tested with Ubuntu):  
`curl https://pyenv.run | bash`  

After that you have to add the following lines to your `vim ~/.bashrc` fileend:
```bash
#Pyenv loader
export PYENV_ROOT="$HOME/.pyenv"
[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"

# Load pyenv-virtualenv automatically
eval "$(pyenv virtualenv-init -)"

```   

To take this changes into effect you have to restart your terminal or run `source ~/.bashrc`. Now it is ready to go.


#### Useful commands
| **command**            	| **description**                                                                                 	|
|---------------------------|-------------------------------------------------------------------------------------------------	|
| `pyenv install --list` 	| all possible python versions to install.                                                        	|
| `pyenv install <version>` | install the choosen <version> from --list. This can take a while...                             	|
|    `pyenv versions`    	| shows all installed environments and the active one                                             	|
|         `pyenv`        	| help site                                                                                       	|
|  `pyenv global <system>` 	| Don't use this, if you not sure what you are doing. We will use poetry for the python versions. 	|




### Poetry
Poetry takes care of the python versions and the packages. All this is handled in a single *.toml file.
Changes can be done in this file, but mainly it is recommended to use the terminal.

#### Installation
Pip is the package manager for python. For poetry it is recommended to install it with pipx, which takes care of the packages globaly.  
1. Install [pipx](https://pipx.pypa.io/stable/installation/)
```bash
sudo apt update
sudo apt install pipx
pipx ensurepath
```

2. install [poetry](https://python-poetry.org/docs/#installation)
```bash
pipx install pipx
```

#### Useful commands
| **command**                  	| **description**                                                    	|
|------------------------------	|--------------------------------------------------------------------	|
|       `poetry install`       	| all possible python versions to install.                           	|
|         `poetry init`        	| This folder will set up to use a virtual environement with poetry. 	|
|  `poetry new <projectname>`  	| Makes the folder with the files in it.                             	|
| `poetry add <pythonpackage>` 	| Add a package to your project.                                     	|
|       `poetry install`       	| Have to be run, befor running the code.                            	|