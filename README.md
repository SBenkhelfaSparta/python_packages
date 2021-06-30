# Building Python Packages
## What is Python Package and benefits
### Structure 

- step 1 ` create an app folder `
- step 2 inside app folder `__init__.py` empty - to initialise our package
- step 3 inside app folder `fizzbuzz.py` add our functionality 
- step 4 `program.py` on dir level - to use as our run file
- `setup.py` on a dir level - to describe our module details such as version, author and contact details


```
building_python_packages
-- app
--- __init__.py
--- fizzbuzz.py
program.py
setup.py
``` 

- Let's build our package starting with `setup.py`
```python
from setuptools import setup

# Let's add some information about your package
setup(name="app")
version = "1.0"
description = "Python app"
author = "Salem at Sparta Global"
author_email = "salem@fakemail.com"
url = "https://www.spartaglobal.com"
```
- code for `fizzbuzz.py`
```python
class FizzBuzz:
    def fizzbuzz(self, fizz, buzz):
        for fizzbuzz in range(100):
            if fizzbuzz % 3 == 0 and fizzbuzz % 5 == 0:
                print(fizz+buzz)
                continue
            elif fizzbuzz % 3 == 0:
                print(buzz)
                continue
            elif fizzbuzz % 5 == 0:
                print(buzz)
                continue
            print(fizzbuzz)
```
- code for `program.py`
```python
from app.fizzbuzz import FizzBuzz

one_to_100 = FizzBuzz()

print(one_to_100.fizzbuzz("beep", "boop"))
```

- ` pip install .` to install our package using `pip` package manager