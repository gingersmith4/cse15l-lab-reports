# Lab Report 1 Week 2

### Installing VS Code
- Go to the VS Code website using [this link](https://code.visualstudio.com)
- Follow any instructions to set it up on your computer 
![vscode](/vscode.png)

### Remotely Connecting
- First find your username and reset your password at [this link](https://sdacs.ucsd.edu/~icc/index.php) and (this is very important) **don't use Safari!** It probably won't work so use a different browser. Your password will take about 15 minutes to be reset.
- Open a terminal in VSCode, do this by clicking terminal at the top bar of your screen (shown in the screenshot below) and then click "New terminal."
![terminal demo](/terminal.png)
- Now in the terminal type `ssh cs15lwi22afe@ieng6.ucsd.edu` replacing the "afe" with letters specific to your username. Now you'll be prompted to enter your password (which we reset earlier), when you type or paste it in you won't be able to see it but that's normal, just hit enter and you should see something like this.
![ssh 1](/remote1.png)
![ssh 2](/remote2.png)

### Trying Some Commands 
- Now we'll try out some commands. Try running them both on the client (your computer) and the server (ieng6). To log out of the remote server type "logout" in the terminal or Ctrl-D
- `cd ~`
- `cd`
- `ls -lat`
- `ls -a`
- `ls <directory> where <directory> is /home/linux/ieng6/cs15lwi22/cs15lwi22abc`, where the abc is one of the other group members’ username
- `cp /home/linux/ieng6/cs15lwi22/public/hello.txt ~/`
- `cat /home/linux/ieng6/cs15lwi22/public/hello.txt`
![commands](/commands.png)

### Moving Files with scp
- Now we'll use scp to copy files from your computer to a computer that's remote. The command is `scp` and you run it on your computer (the client).
- Make a file called `WhereAmI.java` on your computer and put this text in it. 

`class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
`

- Run it by using `javac WhereAmI.java` and `java WhereAmI` and see what prints out.
- Now run this command in your terminal, but using your username. `scp WhereAmI.java cs15lwi22afe@ieng6.ucsd.edu:~/` You'll need to enter your password just like when you do `ssh`.
    - You need to open the terminal in the folder where your file is, so if you're not sure if you're there type `ls` into the terminal, if `WhereAmI.java` doesn't show up that means it's not in the same folder as your terminal. To navigate to that folder type `cd <foldername>` and then `ls` again to check that the file is there.
- Now log back in to ieng6 and use `ls` to check if the file is there, you can also run it with `javac` and `java`! See if there's any difference in what is printed out compared to your computer.
![difference](/scp.png)

### Setting Up an SSH Key
- You can use ssh keys as a quicker way to log into the server, it's a little bit like using your fingerprint to unlock your computer but with a picture stored on your computer (the client) to unlock the server.
- We'll use the program `ssh keygen` which creates a public key and a private key, the public key goes on the server and the private key goes on the client (your computer) and those together allow you to login without using your password!
- Type the following and hit enter at enter passphrase, except the file will be different since your computer has a different name. You'll see a picture type thing (made up of symbols) printed out.
`$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/gingersmith/.ssh/id_rsa): /Users/gingersmith/.ssh/id_rsa`
- This made two new files on your computer, the public and private key, now we'll move the **public** key to the server. Login with `ssh`, then type `mkdir .ssh` once you're on the server and then logout. Now (back on the client) type: (replacing the location and username with yours)
`$ scp /Users/gingersmith/.ssh/id_rsa.pub cs15lwi22afe@ieng6.ucsd.edu:~/.ssh/authorized_keys`
![key](/key.png)

### Optimize Remote Running
- Here are some things you can try to make it more convenient to edit a file (like WhereAmI.java) on your computer and copy and run it on the remote server:
    - Use the up arrow to reuse a command you typed earlier in the terminal
    - Use semicolons to run multiple commands on the same line
![optimize](/optimize.png)

Congratulations! You made it to the end of the tutorial!

[Back to home page](index.html)
