# Android setools

## About
This repo contains a bundled Debian package (`deb`) with the patched SELinux libaries (`libsepol`, `libselinux`) and supporting headers (`libbz2`) that allow SE for Android ("SEAndroid") v30 binary policies to be parsed. In addition, it includes a `Makefile` that will build a patched version of `setools` version 4.0.0 that exposes the following SELinux utilities:

* sesearch
* sediff

All other `setools` binaries (such as any GUI compoents are _not tested_.

## Supported Platforms
Building has been testing on:

* Ubuntu 14.04.5 LTS (the recommended distro/version for build AOSP)
* Ubuntu 18.04.1 LTS

You'll also need the following core components:

* make
* git
* python2.7 (python3 is untested)
* gcc (versions 4.8.4 - 7.3.0 have been tested)

## Installing
First, install dependences:

	sudo apt update
	sudo apt install make git swig flex bison python-dev python-setuptools python-networkx

Next, clone this repo and use the bundled `Makefile` to build and install:

	make build
	sudo make install
