# 'cygpkg'

This script list all installed "top-level" Cygwin packages, "top-level" here
means no other packages depend on it.

It's useful when you want to install same set of Cygwin packages again but don't
know what packages are exactly what you want, yes a `cygcheck -cd` will list all
packages installed but most of them are packages installed automatically by
dependencies and we don't really care about them.

# How does it work

It reads package dependencies from `setup.ini` file and get list of currently
installed packages from `cygcheck -cd`, then finds out packages that no one
depends on, that's all.

# Usage

`cygpkg < setup.ini`
