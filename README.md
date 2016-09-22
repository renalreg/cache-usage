# Caché Usage

A script for reporting information about Caché databases (size, free space, etc.).
Run with `--help` for the list of available columns.

## Requirements

* Python 2.7
* [Caché Python bindings](http://docs.intersystems.com/latest/csp/docbook/DocBook.UI.Page.cls?KEY=GBPY_intro)

## Usage

All databases:

```
cache-usage
```

Specific databases:

```
cache-usage /opt/hs/mgr/user/
```

For more options see `--help`:

```
cache-usage --help
```

## RHEL 6

```
alias cache-usage='LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/opt/hs/bin scl enable python27 -- cache-usage --username YOUR_USERNAME --password YOUR_PASSWORD'
```

RHEL 6 has Python 2.6 installed by default so we use `scl` to run the script with Python 2.7.
The `LD_LIBRARY_PATH` is updated so `libcbind.so` is on the path.
The `--username` and `--password` arguments are provided for convenience.
The alias assumes the `cache-usage` command is on the PATH (e.g. `/usr/local/bin`).

## License

Copyright (c) 2016 UK Renal Registry.

Licensed under the [MIT](LICENSE.txt) license.
