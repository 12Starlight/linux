# **Upgrading Software**

Overtime, software becomes `outdated` as newer versions are released and new functionality is produced.

The apt package manager has a very elegant way of using the package lists in your `apt-cache` to ensure that all the software on your system is fully up to date.

Doing so not only makes your software more `functional` and `modern`, but it also enhances system `security`.

To update all the software on your system to the most up-to-date versions mentioned in the package lists in your apt-cache use:

&nbsp; &nbsp; &nbsp; &nbsp; `sudo apt-get upgrade`

Bc this process uses the package lists in your apt-cache, in order for this to be effective, your package lists should be completely up-to-date.

Therefore, *`you must ensure that your package lists are up to date before upgrading software`* by using:

&nbsp; &nbsp; &nbsp; &nbsp; `sudo apt-get update`

**`Note:`** This only update software installed via the package manager. It will not work for software compiled and installed manually. Therefore, *`always aim to install software from the repositories wherever possible.`*

&nbsp;

# **Installing Software**
Installing software is a very easy task using the `apt` package manager.

When you have found a package that you would like to install simply do:

&nbsp; &nbsp; &nbsp; &nbsp; `sudo apt-get install <package name>`

This will download and install the package, as well as any dependencies that are required in order to make the package function.

Again, in order to install the most up to date version of the package, *`ensure that you have updated your cache prior to installing`* by executing `sudo apt-get update`.