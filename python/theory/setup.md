## Links:

1. How to think like Computer Scientist: https://runestone.academy/runestone/books/published/thinkcspy/index.html

2. 

## Useful Applications:

1. 

## Useful Plugins:

## Create a virtual environment

To create a virtual environment, go to your project’s directory and run venv. If you are using Python 2, replace venv with virtualenv in the below commands.

```
python3 -m venv env
```

The second argument is the location to create the virtual environment. Generally, you can just create this in your project and call it env.

*venv* will create a virtual Python installation in the env folder.

Activating a virtual environment will put the virtual environment-specific python and pip executables into your shell’s PATH.

```
source env/bin/activate
```

You can confirm you’re in the virtual environment by checking the location of your Python interpreter, it should point to the env directory.

```
which python
.../env/bin/python
```

If you want to switch projects or otherwise leave your virtual environment, simply run:

```
deactivate
```

The above modules can be installed with one pip command.

```
pip install pandas scipy scikitlearn statsmodels sympy matplotlib jupyter
```

## GitHub Basics

-Before creating a new branch, pull the changes from upstream. Your master needs to be up to date.
```
git pull
```

-Create the branch on your local machine and switch in this branch :

```buildoutcfg
$ git checkout -b [name_of_your_new_branch]
```

- Add your changes

```buildoutcfg
git add .
```

```buildoutcfg
git commit -m "comments"
```

-Push the branch on github :

```buildoutcfg
$ git push origin [name_of_your_new_branch]
```

- When you want to commit something in your branch, be sure to be in your branch. Add -u parameter to set upstream.

- You can see all branches created by using :

```buildoutcfg
$ git branch -a

```

