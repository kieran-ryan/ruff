 ## TODO

- Replace pip installs with uv commands
- Are there any other file names that will trigger a violation

## Project

```console
my_project
└── src
    └── implicit
        └── baz space.py
```

## ruff (N999)

```console
$ pip install ruff
$ ruff check src/implicit/ --select=N999
All checks passed!
```

## flake8 (N999)

```console
$ pip install flake8 flake8-module-name
$ flake8 src/implicit/ --select=N999
src/implicit/baz space.py:0:1: N999 filename should be all lower case
```

## pylint (C0103)

```console
$ pip install ruff
$ pylint src/implicit/ --enable=C0103
************* Module file name
crates/ruff_linter/resources/test/fixtures/pep8_naming/N999/module/implicit_namespace/file name.py:1:0: C0103: Module name "file name" doesn't conform to snake_case naming style (invalid-name)
```
