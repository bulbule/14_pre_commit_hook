# Quadratic Equations Solver
This repo contains a script `quadratic_equation.py` that solves quadratic equation in real numbers as well as the `tests.py` to it.
When commiting a new version of `quadratic_equation.py` it is possible to run the `tests.py` automatically. If the tests break, the commit will not take place. To do that, one needs to add the file `pre-commit` into `./git/hooks`.

# Usage
The example shows that in the current form `quadratic_equation.py` does not comply with our tests and an error occur when trying to commit.
```#!bash
$ git commit -m "initial commit"
.E..
======================================================================
ERROR: test_returns_none_for_complex_solution (__main__.QuadraticEquationTestCase)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "tests.py", line 22, in test_returns_none_for_complex_solution
    root1, root2 = get_roots(1, 2, 3)
  File "/Users/anyya/python/devman/14_pre_commit_hook/quadratic_equation.py", line 5, in get_roots
    root1 = (-b - sqrt(discriminant)) / (2 * a)
ValueError: math domain error

----------------------------------------------------------------------
Ran 4 tests in 0.002s

FAILED (errors=1)
> Tests DID NOT pass

```

# Project Goals

The code is written for educational purposes. Training course for web-developers - [DEVMAN.org](https://devman.org)
