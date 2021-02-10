# **Searching the Cache**

Ubuntu's package manager (`apt`) uses the `/var/lib/apt/lists` as a `cache`. A cache is basically a place to store a local copy of some files in order to improve computational performance.

This cache (known as the `apt-cache`) contains lists of packages available in the Ubuntu repositories.

&nbsp;

The `Ubuntu Repositories` are:

| Name             | Description                                             |
|:---              |:---                                                     |
| **`Main`**       | `Free and Open Source` Software maintained by Canonical |
| **`Universe`**   | `Free and Open Source` Software maintained by the Ubuntu Community |
| **`Restricted`** | `Proprietary software` and drivers for company-specific devices such as wireless cards etc. |
| **`Multiverse`**  | Software that is `restricted either by copyright or legal issues`.

&nbsp;

To search the `apt-cache` for packages that match a certain search term you can use:

&nbsp; &nbsp; &nbsp; &nbsp; `apt-cache` search `<search term>`

This will list out all the packages that match a certain search term, and also give a snippet of information about each result.

To find more information about a specific package you can do:

&nbsp; &nbsp; &nbsp; &nbsp; `apt-cache` show `<package name>`

&nbsp;

# **Updating the Cache**

There is a configuration file called `sources.list` located in the `/etc/apt` directory that tells the package manager which package lists to download.

These package lists are stored on archive.ubuntu.com

An important factor for maintaining any cache is to insure that it is up to date with the original source, and `updating your systems cache` is fortunately very easy to do.

Just do:

&nbsp; &nbsp; &nbsp; &nbsp; `sudo apt-get update`

This will cause the apt package manager to compare your package lists in your cache to those available on archive.ubunto.com and ensure you have the most up to date versions.