## Install Pycharm in Linux

Pycharm is one of the most popular and beat IDE for python development. It is available in two different versions one is Professional and another is Community. Community version is totally free to use.
There are many different ways to download pycharm for Linux, Here I will show some methods how to install pycharm.

**1.Install via snap**

This is the easiest way to install Pycharm in Linux, But snap is not available in all Linux distro. So before install pycharm, you need Snap. In Ubuntu, Manjaro, Lubuntu snap pre-installed. To install snap open terminal and type bellow commands

```
$ sudo apt install snapd
``` 
Not install Pycharm via snap 

```
$ sudo snap install pycharm-community --classic #for community edition
$ sudo snap install pycharm-professional --classic #for professional edition
``` 
To install snap in Linux Mint need to remove nosnap.pref to do it run the following command

```
$ sudo rm /etc/apt/preferences.d/nosnap.pref
$ sudo apt update
``` 
**2.Install from official website**

This is recommended way to install pycharm, Intellij, Androistudio, and other JetBrains IDE. To install need to download the tar file from JetBrains *https://www.jetbrains.com/pycharm/download/#section=linux*
next, run this commands

```
$ cd Downloads #Change directory to download
$ ls
# copy downloaded tar filename
$ tar -xfz pycharm-professional-2021.1.1.tar.gz
$ cd pycharm-professional-2021.1.1
$ cd bin
$ chmod u-x pycharm.sh #allow executing permission
$ sudo ./pycharm.sh #execute this
``` 

![Screenshot from 2021-05-29 15-30-17.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622282438480/BDqcCGpvP.png)

![Screenshot from 2021-05-29 15-31-03.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622282651857/88w3RZ-c9.png)
Now agree with JetBrains' terms and conditions. After this, it will show Pycharm welcome page. Click on the setting and select "Create Desktop Entry" this will create a desktop shortcut.

![Screenshot from 2021-05-29 15-32-48.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622282672357/YfkfIw3iG.png)

![Screenshot from 2021-05-29 15-33-10.png](https://cdn.hash	node.com/res/hashnode/image/upload/v1622282676510/uSmjIXWNw.png)

**3.Install Via JetBrains Toolbox App**
If you want to download not only Pycharm also other JetBrains apps like Android Studio, IntelliJ, etc this will help to download all of them. To download Toolbox go to Jetbrains product page *https://www.jetbrains.com/products/* download from there or click here to download *https://www.jetbrains.com/toolbox-app/download/download-thanks.html*

```
$ cd Downloads
$ tar -xfz jetbrains-toolbox-1.20.8352.tar.gz
$ cd jetbrains-toolbox-1.20.8352
$ ./jetbrains-toolbox
``` 
After this Toolbox will open. From there select pycharm and download after some time it will download and install automatically. This toolbox can update all apps automatically.
If anything wrong here please let me know..