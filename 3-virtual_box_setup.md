# Virtual Box Setup:

Setting up VirtualBox on your Ubuntu 22.04 system involves a few steps. Here's a step-by-step guide to get you started:

## Step 1: Update Your System:

Before installing any new software, it's a good idea to update your system. Open a terminal and run:

<pre>

sudo apt update
sudo apt upgrade
</pre>

## Step 2: Add Oracle VirtualBox Repository:

Since VirtualBox is not included in the default Ubuntu repository, you need to add the Oracle repository.

+ Add Oracle's GPG key:
    <pre>

    wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
    </pre>

+ Add the VirtualBox repository:
    <pre>

    sudo add-apt-repository "deb [arch=amd64] https://download.virtualbox.org/virtualbox/debian $(lsb_release -cs) contrib"
    </pre>


## Step 3: Install VirtualBox:

Once the repository is added, install VirtualBox by running:
<pre>

sudo apt update
sudo apt install virtualbox-7.0
</pre>
(Replace 7.0 with the latest version if needed.)

## Step 4: Install Extension Pack (Optional but Recommended):

The VirtualBox Extension Pack adds useful features like USB 2.0/3.0 support, RDP, etc.

+ Download the Extension Pack from the VirtualBox website.

+ Install the Extension Pack using VirtualBox:

    + Open VirtualBox.
    + Go to File > Preferences > Extensions.
    + Click the "Add" button and select the downloaded Extension Pack.

Alternatively, you can install it via the terminal:
<pre>

sudo VBoxManage extpack install /path_to_extension_pack
</pre>

## Step 5: Add Your User to the vboxusers Group
To use USB devices in VirtualBox, you need to add your user to the vboxusers group:

<pre>

sudo usermod -aG vboxusers $(whoami)
</pre>

## Step 6: Verify Installation:

Once installed, you can open VirtualBox from the application launcher or by typing:
<pre>

virtualbox
</pre>



## To learn more:
Video link:

[virtual box setup](https://www.youtube.com/watch?v=4j2juiMJIhg&list=PL0tP8lerTbX3eUtBFS0Ir4_aFqKuXWjYZ&index=3)