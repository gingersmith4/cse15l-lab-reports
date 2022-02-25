# Lab Report 3 Week 6

## Copying whole directories with `scp-r`

# Copying markdown-parse directory into ieng6 account

![copying directory](/copyDirect1.png)
![copying directory continued](/copyDirect2.png)

# Logging into ieng6 and compiling and running tests

![running tests](/runOnRemote.png)

# Combining `scp, ;, ssh` to copy the whole directory and run the tests in one line.

This is the command I used: 

`scp -r markdown-parse cs15lwi22afe@ieng6.ucsd.edu:~/mdparse-lab3; ssh cs15lwi22afe@ieng6.ucsd.edu "cd md-parse-lab3; bash mdparse"`

`scp -r` means recursively transfer the following directory to in this case ieng6.

`mdparse-lab3` creates a directory to put this in since a markdown-parse directory already exists.

`ssh` is to log in to the remote server.

`"cd md-parse-lab3; bash mdparse"` changes into the directory we just made and then runs the commands in the bash file. The bash file is show below and makes it easier to run.

mdparse file:
![combo](/screenshot-mdparse.png)

Combined command:
![combo](/combo-command.png)

Result once you scroll to the bottom:
![combo](/result.png)

[Back to home page](index.html)
