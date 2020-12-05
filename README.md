# Framework-Functionnal-Test-python
A quick and dirty pytest plugin to test command line programs given YAML
specifications.


This file comes with absolutely no warranties and support will only be
best-effort. You're encouraged to hack on it, though.

Drop it (still named conftest.py, this is important) at the root of your
functional tests directory, and run with "pytest" from the root of your
project.

Starting from the directory containing this file, and recursively through all
sub-directories, all files ending with ".yaml" will be collected, no matter
their name.
