# Framework-Functionnal-Test-python
A pytest plugin to test command line programs given YAML
specifications.

Drop it (still named conftest.py, this is important) at the root of your
functional tests directory, and run with "pytest" from the root of your
project.

Starting from the directory containing this file, and recursively through all
sub-directories, all files ending with ".yaml" will be collected, no matter
their name.
## Installation Process

* Create a virtualenv with "python -m venv venv"
* Activate the virtualenv with "source venv/bin/activate"
* Install the dependencies with "pip install pytest pyyaml"
* The virtualenv directory should not be commited, add it to your gitignore

## Yaml files configuration
Here is an example yaml:

name: cat should have identical stdin and stdout
command: cat
stdin: |
foobar
barfoo
stdout: |
foobar
barfoo
---
name: failing for all three reasons
command: echo "foo"
stderr: |
machin
returncode: 1

Two noteworthy things, if you're not familiar with YAML:
* Multiple yaml items can be defined in a single file, as long as they are
separated by "---".

* Multiline values are done by adding a pipe.
See https://yaml-multiline.info/ to learn more about the syntax.

