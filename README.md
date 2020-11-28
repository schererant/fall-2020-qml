## Install dependencies

Install python dependencies from Pipfile.lock in a new virtualenv (this might take some time)

```buildoutcfg
pipenv install
```


Start a pipenv shell. Inside this shell is where your dependencies from the previous step were installed. The dependencies can only be accessed inside the shell.  
   
```buildoutcfg
pipenv shell
```

## Start jupyter notebook in lab

Once instide the shell, start a jupyter notebook. This should open a jupyter lab notebook environment in a browser:

```buildoutcfg
jupyter lab
```

If you prefer jupyter notebook (old style stuff):
```buildoutcfg
jupyter notebook
```


## Install a new python package 

If you need a new package, there are 2 ways to do it. 

### Add package to Pipenv file manually

Open the Pipenv file and add the package name and version. Then run this command (outside the pipenv shell). This will update the lock file

```buildoutcfg
pipenv update
```

### Add package from command line

In the command line (outside the pipenv shell), add the package directly running this command:

```
pipenv install mypackagename==1.2.3
```


## Final remarks

Clean notebook outputs before commit:

```buildoutcfg
jupyter nbconvert --clear-output --inplace qubit-operations.ipynb
```
