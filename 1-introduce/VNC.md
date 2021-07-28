# Set VNC

## Connect myagv desktop remotely using VNC

See here you may have questions, myAGV is free to walk around, if always connected to a screen, how to gallop.
Here we can use VNC to solve this problem with the remote desktop.

VNC (Virtual Network Console) is an abbreviation for the Virtual Network Console. It is an excellent remote control tool software, VNC is free open source software based on UNIX and Linux operating systems, powerful remote control, efficient and practical. VNC basically consists of two parts: part is client's application (vncviewer); the other is server-side application (vncserver).


**1.Install vncserver in myAGV's system**
1. First open a console terminal (shortcut <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>T</kbd>), enter the following instructions to update the software source library:

```c
sudo apt-get update 
```
2. Install VNCserver, Enter the following command at the terminal:

```c
sudo apt-get install vnc4server
```
3. Start vnc4server, Enter the following command at the terminal:

```c
vnc4server
```

You are prompted for a password, which will be used when linked through the client.

When you enter the password, you will see a prompt similar to the following side:
> New ‘3 ()’ desktop is ****:3 (****代表主机名） Take notice of the number
> after the colon (, in this case it is “3.”


One will occur in your home directory after starting the vnc4server. Directory of the vnc.

This is now possible to link to the server via the vnc client.

**2.Install the VNCviewer on your computer**

Open the browser and go to the website:
[https://www.realvnc.com/en/connect/download/viewer/](https://www.realvnc.com/en/connect/download/viewer/)

Select the system corresponding to the computer, and download the installation file.

![VNC网页](../image/小车初次使用/vnc网页.png)

Start the installation, the language can choose English, German, French, Italian and Western, click ok to go to the next step:

![VNC安装1](../image/小车初次使用/vnc安装1.png)

Then keep clicking "next", using the default settings.
![VNC安装2](../image/小车初次使用/vnc安装2.png)

**3.Remote connection of computer to myAGV desktop**

First enter in the terminal command line of the myAGV: **ifconfig** to check the IP address of the myAGV, where I must address 192.168.123.22.22. The IP address changes dynamically and changes with different WIFI connection, so after each startup, it is recommended to check the IP address to confirm any change.
![VNC连接1](../image/小车初次使用/vnc连接1.png)

Open the vncviewer client on the computer side, enter the myagvoip address we just read in the top small window, and then press enter.
![VNC连接2](../image/小车初次使用/vnc连接2.png)

Click on the word "continue"

![VNC连接3](../image/小车初次使用/vnc连接3.png)

Enter the password of the VNCserver we set on the myAGV, it is recommended to check "Remember password" does not need to enter the password the next time you log in. Then click on "ok"
![VNC连接4](../image/小车初次使用/vnc连接4.png)

It's done. Now we can remotely connect myAGV's desktop on the computer and control it.

![VNC连接5](../image/小车初次使用/vnc连接5.png)