# Update MacPorts: Keeping MacPorts packages updated

This package installs a script that maintains MacPorts packages. The script is invoked by MacPorts package `anacron`.

# Installation

```
$ ./configure
$ make
$ make install
```

`make install` will invoke sudo for commands that require privileges, so don't be suprised when it asks for a password.

# Reconfiguring

If you change the configuration at `configure.ac`, re-build the `configure` script:

```
$ make -f configure.mk
```

