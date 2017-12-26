# How to Install and Use Atom for Mac

In this tutorial I'm going to show you how install and use `Atom` to edit your code on your personal computer. `Atom` has a betuiful graphical interface which makes it *much easier* to edit your code! There are many `text editors` out there, so if you like on better than `Atom` feel free to use that. The same general steps should work for any `text editor`.

## Step 1: Download

Download `Atom` [here](https://atom.io/)

## Step 2: Install

Once `Atom` has downloaded, click the file to open the installer. The install should only take about a minute and should automatically open `Atom` after it is done.

The `Atom` editor allows you to edit any `.c` file and provides really nice feature like auto-completing coding that makes coding a joy!

## Step 3: Connect to Purdue Servers

All your files for `CS 159` are stored on the `ITAP guru` servers (when you use `PuTTY`, you are connecting to their servers.

To connect to `guru` on your Windows machine, you must first be connected to Purdue's network, `PAL`. If you are not on PAL (i.e. you are not on campus, or don't live in the dorms), you must connect to PAL using a [VPN](https://cla.purdue.edu/facultyStaff/it/documents/Instructions/Connect%20to%20Purdue%20VPN%202015%20Windows.pdf).

Once you are connected to `PAL` go to find and click `Go -> Connect to Server`, or just press `Command-K`

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/goButton.png)

Enter `smb://myhome.itap.purdue.edu/myhome/username` in the `Server Address:` field, where `username` is your `Purdue career account username`.

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/connectToServer.png)

Press the `+` button to save it this server to easily connect later.

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/saveServer.png)

From this menu, click `Map network drive` and then click on `Map network drive` from the sub-menu. That will bring up this window:

If prompted, enter your username as `onepurdue\username` where `username` is your `purdue career account username` and your password as your `purdue career account password`

Once it connects, a window should pop up with your `career account drive` on it.

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/connected.png)

From here you can go into the `CS159` folder and it will contain all your labs and homeworks. So for example, if you wanted to open lab 0 in `Atom`, simply go to the `lab00` folder, and right click on `lab00.c`. 

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/rightClickOpen.png)

Select `Open with -> Atom`. It should look something like this:

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/atomMac.png)

Enjoy your `PuTTY` free life!*

*(Note: you can use this method to open your lab in `notepad++` on the windows computers in lab. You will still need putty open to compile your files)

## Step 4 Logging into Guru on your Mac

Since you still need to compile your code, you'll still need to get on a terminal and connect to the `guru` server, lucky for you, you have a `Mac`, which has a built in `UNIX` terminal (`Windows` does not, which is why you have to use `PuTTY`).

Simply open the `terminal` app from your Mac, and type `ssh username@guru.itap.purdue.edu` where `username` is your `Purdue career account username`. Terminal will prompt you for your password, and you will enter it just like you do in lab. 

Now you are connected to `guru`. Now you can use the terminal just like you would use `PuTTY`. 