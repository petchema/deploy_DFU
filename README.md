deploy_DFU
==========

This script can be used to automate the installation of Daggerfall Unity,
and lots of mods. I use it daily for my own testing needs.

REQUIREMENTS
============

The script depends on the following external archivers:

- unzip
- unrar
- 7z

SCRIPT INSTALLATION
===================

Put the script in some directory where it will be easy to run; If necessary
make it executable (chmod +x deploy_DFU).

CONFIGURATION
=============

- Copy sample.deploy_DFUrc as ~/.deploy_DFUrc before editing it with your
favorite text editor;

- Modify the directory where deploy_DFU will find all the installation
archives; Since there's no generic way to download all the mods, you will
have to download all the archives on your own.

- Select the options you want, for example change =N to =Y after the
mods you want to install.

USAGE
=====

When this is done, run

    $ deploy_DFU <target_directory>

"target directory" should be either a directory that doesn't exist
yet, or a previous installation done by deploy_DFU, in which case the
installation will be *replaced*.

If no issues are detected (missing archivers, missing or incorrect
configuration file, missing archives,...) this should start installing
Daggerfall Unity and the mods you selected:

ADVANCED USAGE
==============

You can have several configuration files, for example for testing
purposes. All you need to do is call deploy_DFU like:

    $ deploy_DFU -f <config file> <target directory>
