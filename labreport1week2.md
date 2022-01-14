# Week 2 Lab Report

## Installing VSCode
***
In order to get [VSCode](https://code.visualstudio.com/), you must first access the website by clicking on the hyperlink or searching it up on your web browser. Second, once you are on the site, there should be a download button; it should detect if you're on Mac, Windows, or Linux, but clicking on the arrow next to it should bring up different versions of installers that you can use for your operating system. 
![Image](/Screenshots/vscode website.jpg)

Upon pressing it, you should be redirected to another part of their website and the download of the installer should start automatically. 
![Image](/Screenshots/vscode download starting automatically.jpg)

Once the download is done, open the installer and follow the steps it provides and it should be installed soon after.
![Image](/Screenshots/vscode installer.jpg)

[VSCode Redirect](https://code.visualstudio.com/)

## Connecting Remotely
***
To connect remotely to the CSE servers, OpenSSH will be used. For Windows, make sure that it is installed by following this [guide](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse).

Afterwards, determine which account you will be logging into on the servers by looking up the account name [here](https://sdacs.ucsd.edu/~icc/index.php). You will need your PID and username. When you press submit, it will take a few moments but the CSE server accounts should appear along with which courses they are associated with. If this does not work, try the second part where you will need your last name and PID. Logging on for the first time, it is suggested to reset your password for these accounts as well.
![Image](/Screenshots/account lookup.jpg)

Once you get your CSE server account name for CSE15L, it should look like something along the lines of ```cs15lwi22???```(for Winter quarter, 2022 that is), with the three question marks being your account name. Now open VSCode and then open a terminal, which can be done through the shortcut ``` command/ctrl + ` ```. Then use the ssh command to log in, ```ssh cs15lwi22???@ieng6.ucsd.edu```. The ```@ieng6.ucsd.edu``` part is like an address for their servers. Trying to log on for the first time, it may point out how the authenticity of the host cannot be established. This only appears once and it's okay to disregard it by responding ```yes``` to it, however if it keeps appearing, the connection is most likely being altered in some way. Afterwards, it should prompt you to enter a password, so enter the password from when you reset it. It may look like nothing is being written down while typing, but that's normal. If issues arise, make sure you entered it correctly or wait a bit after resetting it, it takes a bit of time for changes to take place. To log out from the server, just use the command ```logout```.

This is what it should look like once you are logged in.

![Image](/Screenshots/sshcommand.png)

## Trying Some Commands
***
Now while you're connected to the server, here is a list of *some* commands you could run:
-```cd```: stands for change directory, a command to change your current directory
-```cd ~```: makes your current directory the home directory
-```ls```: lists out the contents of your current directory
-```ls -lat```: lists out the contents of your current directory with **hidden** directories and files included.
-```ls <directory>```: lists out the contents of the directory provided
-```cat <file directory>```: prints out the contents of the file
-```mkdir```: creates a directory or directories

![Image](Screenshots/examples of commands.jpg)

## Moving Files with ```scp```
***

## Setting an SSH Key
***

## Optimising Remote Running 
*** 

