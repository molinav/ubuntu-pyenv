# Docker-PyEnv

This repository creates GNU/Linux Docker images with a specific Python version
using [PyEnv]. Current tested base images include [Ubuntu 20.04], [CentOS 7]
and [openSUSE 15.3].


## Features

The images provide the following libraries:

- GCC and GFortran.
- BLAS and LAPACK.
- HDF4, HDF5 and NetCDF4.
- PyEnv with one specific Python version preinstalled.
- Latest available working versions of [`pip`], [`wheel`] and [`setuptools`].
- Latest available working versions of [`numpy`], [`scipy`] and [`cython`].

Below there is a summary table with the preinstalled packages:

| Version    | Py2.6  | Py2.7  | Py3.2  | Py3.3  | Py3.4  | Py3.5   | Py3.6   | Py3.7+  |
|------------|--------|--------|--------|--------|--------|---------|---------|---------|
| pip        | <10    | <21    | <7.1.1 | <18    | <20    | <21     | <21     | <21     |
| setuptools | <37    | <45    | <30    | <40    | <44    | <50     | <50     | <50     |
| wheel      | <0.30  | <0.36  | <0.32  | <0.30  | <0.34  | <0.36   | <0.36   | <0.36   |
| numpy      | <1.12  | <1.17  | <1.12  | <1.12  | <1.17  | <1.19   | <1.20   | <1.21   |
| scipy      | <0.18  | <1.3   | <0.18  | <1.0   | <1.3   | <1.5    | <1.6    | <1.7    |
| cython     | <3.0   | <3.0   | <0.27  | <3.0   | <3.0   | <3.1    | <3.1    | <3.1    |


## Installation

1. Install [Docker].

2. Download the automated build from the public [Docker Hub Registry]
   located at [molinav/pyenv].


## Usage

Given a Python version `X.Y`:
```sh
docker run --rm -it molinav/pyenv:X.Y-ubuntu-20.04
docker run --rm -it molinav/pyenv:X.Y-centos-7
docker run --rm -it molinav/pyenv:X.Y-opensuse-15.3
```

If not running interactively, you must configure the shell manually by calling
```sh
. /etc/profile
```
which will activate [PyEnv] and configure the shell to use the preinstalled
Python version.


[Ubuntu 20.04]:
https://hub.docker.com/_/ubuntu
[CentOS 7]:
https://hub.docker.com/_/centos
[openSUSE 15.3]:
https://hub.docker.com/r/opensuse/leap
[PyEnv]:
https://github.com/pyenv/pyenv
[`pip`]:
https://pypi.org/project/pip/
[`setuptools`]:
https://pypi.org/project/setuptools/
[`wheel`]:
https://pypi.org/project/wheel/
[`numpy`]:
https://numpy.org/
[`scipy`]:
https://scipy.org/
[`cython`]:
https://cython.org/
[Docker]:
https://www.docker.com/
[Docker Hub Registry]:
https://hub.docker.com/
[molinav/pyenv]:
https://hub.docker.com/r/molinav/pyenv
