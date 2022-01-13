# Lab Report 1 Week 2

### Installing VS Code
- Go to the VS Code website using [this link](https://code.visualstudio.com)
- Follow any instructions to set it up on your computer 

### Remotely Connecting
- First find your username and reset your password at [this link](https://sdacs.ucsd.edu/~icc/index.php) and (this is very important) **don't use Safari!** It probably won't work so use a different browser. Your password will take about 15 minutes to be reset.
- Open a terminal in VSCode, do this by clicking terminal at the top bar of your screen (shown in the screenshot below) and then click "New terminal."
![terminal demo](/terminal.png)
- Now in the terminal type `ssh cs15lwi22afe@ieng6.ucsd.edu` replacing the "afe" with letters specific to your username. Now you'll be prompted to enter your password (which we reset earlier), when you type or paste it in you won't be able to see it but that's normal, just hit enter and you should see something like this.
![ssh 1](/remote1.png)
![ssh 2](/remote2.png)

### Trying Some Commands 
- Now we'll try out some commands. Try running them both on the client (your computer) and the server (ieng6). To log out of the remote server type "logout" in the terminal or Ctrl-D
- cd ~
- cd
- ls -lat
- ls -a
- ls <directory> where <directory> is /home/linux/ieng6/cs15lwi22/cs15lwi22abc, where the abc is one of the other group members’ username
- cp /home/linux/ieng6/cs15lwi22/public/hello.txt ~/
- cat /home/linux/ieng6/cs15lwi22/public/hello.txt
![commands](/)

### Moving Files with scp

### Setting Up an SSH Key

### Optimize Remote Running

![Screenshot of my website](/exampleScreenShot.png)

[Back to home page](index.html)
