# Caché Usage

A script for reporting information about Caché databases (size, free space, etc.).
Run with `--help` for the list of available columns.

## Requirements

* Python 2.7
* [Caché Python bindings](http://docs.intersystems.com/latest/csp/docbook/DocBook.UI.Page.cls?KEY=GBPY_intro)

## Usage

```
cache-usage --help
```

## RHEL 6

```
alias cache-usage='LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/opt/hs/bin scl enable python27 -- cache-usage --username YOUR_USERNAME --password YOUR_PASSWORD'
```

RHEL 6 has Python 2.6 installed by default to we use `scl` to run the script with Python 2.7.
The `LD_LIBRARY_PATH` is updated so `libcbind.so` is on the path.
The `--username` and `--password` arguments are provided for convenience.
The alias assumes the `cache-usage` command is in the PATH (e.g. `/usr/local/bin`).
