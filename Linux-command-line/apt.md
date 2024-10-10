# apt

apt is a package management command-line tool used in Debian-based systems (like Ubuntu) to handle software installation, upgrade, and removal. It is a simplified front-end to other package management tools like dpkg, apt-get, and apt-cache. It streamlines package management by combining various functions into one command.

## Usage

apt is used to manage software packages, such as installing, updating, removing, and searching for packages.

## Syntax

<pre>apt [option] [package_name]
</pre>

## Common Options:

+ update: Updates the list of available packages and their versions. It does not install or upgrade any packages.

<pre>
sudo apt update
</pre>


+ upgrade: Installs the latest versions of all packages currently installed on the system.

<pre>
sudo apt upgrade
</pre>

+ install: Installs the specified package.

<pre>
sudo apt install "package_name"
</pre>

+ remove: Removes the specified package from the system.


<pre>sudo apt remove "package_name"</pre>

+ autoremove: Removes any packages that were automatically installed to satisfy dependencies for other packages and are no longer needed.

<pre>
sudo apt autoremove
</pre>

+ search: Searches for a package in the repositories.

<pre>
apt search "package_name"
</pre>

+ show: Displays detailed information about a specific package.

<pre>
apt show "package_name"
</pre>

## Difference Between apt and apt-get:

+ apt is a more user-friendly version that combines the functionalities of apt-get and apt-cache into a single command.

+ It provides progress bars and additional helpful prompts during operations.