Keeps track of library versions and allows other machines to easily install them

Example env file: environment yml (for conda or python)
```
name: primes-env
channels:
	- conda-forge
dependencies:
	- python=3.13
	- numpy=2.3
```

Extensions for Python and R
Python: requrirements.txt
R: renv.lock

![[Pasted image 20260929133200.png]]

## Python commands

Create environment
```
python -m venv .venv
```

Install Packages
```
pip install -r requirements.txt
```

Record current versions
```
pip freeze
```

