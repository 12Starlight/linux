# **Installing Source Code**

The `sources.list` file in the `/etc/apt` folder contains lines telling the package manager what package lists it should download.

By default the lines that allow the apt package manager to download source code packages are "commented out" and are preceded by a hash symbol (`#`).

The lines for source code packages start with `deb-src` for example:

&nbsp; &nbsp; &nbsp; &nbsp; `#deb-src gb.archive.ubuntu.com/ubuntu artful main restricted`

To enable source code lists to be accessed by your package manager, open the configuration file using `sudo nano /etc/apt/sources.list` and remove the hash symbol from the front of each line so that for example:

&nbsp; &nbsp; &nbsp; &nbsp; `#deb-src gb.archive.ubuntu.com/ubuntu artful main restricted`

Would become

&nbsp; &nbsp; &nbsp; &nbsp; `deb-src gb.archive.ubuntu.com/ubuntu artful main restricted`

Once done for all lines starting with `deb-src`, you should save the file and update your cache so that the new source package lists can be downloaded.

Update your cache using:

&nbsp; &nbsp; &nbsp; &nbsp; `sudo apt-get update`

Once these new lists are downloaded in your cache, there is one more step to allow you to download source code.

You need to install the `dpkg-dev` package using:

&nbsp; &nbsp; &nbsp; &nbsp; `sudo apt-get install dpkg-dev`

Once that is installed, you are now ready to download source code from the Ubuntu Repositories.

To download source code, simply do:

&nbsp; &nbsp; &nbsp; &nbsp; `sudo apt-get source <package name>`

&nbsp;

# **Compiling and Installing from Source Code**

