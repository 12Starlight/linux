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

With the source code downloaded, you are free to make your own edits to the code, recompile it and install it on your machine.

To compile and install code written in the `C programming language`, you will need the `Gnu C Compiler (gcc)`, which you can install by running:

&nbsp; &nbsp; &nbsp; &nbsp; `sudo apt-get install gcc`

With the `Gnu C Compiler` installed, the compiler must be `configured` correctly prior to compiling a package.

Inside the package directory, there will be a `configure` file. From within the same directory as the configure file, simply run *`configure`*, and the Gnu C Compiler will be configured.

This will generate a new file in the directory called the `MakeFile`.

In order to operate on the make file, you will need to install one more package using:

&nbsp; &nbsp; &nbsp; &nbsp; `sudo apt-get install make`

When that has installed, then from within the same directory as the `MakeFile`, you can execute the *`make`* command and all the software in the package will be ran through the `Gnu C Compiler` and compiled into binary code ready for installation.

In order to install the compiled binary files, simply run:

&nbsp; &nbsp; &nbsp; &nbsp; `sudo make install`