# How to log into a CSE15L account on ieng6?
This page serves as an instruction on how to log into UCSD CSE15L account

Look up your account here **<https://sdacs.ucsd.edu/~icc/index.php>**

## Step One : Installing Visual Studio Code
1. Click on the following link **<https://code.visualstudio.com/>**
![Image](VisualStudio.png)
Download the corresponding version of Visual Studio Code for your operation system.

2. When you finished downloading, open Visual Studio Code and you should see a layout like this
![Image](VisualStudioTerminal.png)

## Step Two : Remotely Connecting To Your CSE15L Account
Many courses in CSE use course-specific accounts. These are similar to accounts you might get on other systems at other institutions (or a future job). We’ll see how to use VScode/terminal to connect to a remote computer over the Internet to do work there.

1. For Windows Users :
    - Install [Git for Windows](https://gitforwindows.org/)
    - Once installed, use the steps [In this post](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994) to set up the default terminal to use the newly-installed `Git bash` in Visual Studio Code

2. Connect to your remote computer using terminal :
    - Open a terminal in VScode (Ctrl or Command + \`, or use the Terminal → New Terminal menu option)
    - Your command will look like this `ssh cs15lsp23zz@ieng6.ucsd.edu` but with the `zz` replaced by the letters in your course- specific account.
    - Then you will get the first-time connect message 
        ```
        ⤇ ssh cs15lsp23zz@ieng6.ucsd.edu
        The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
        RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
        Are you sure you want to continue connecting (yes/no/[fingerprint])? 
        ```
        Type yes and press enter, then type in your password.\
        **Attention : when typing your password, your terminal will look like this ![Image](PassWord.png) Your typed in password will not show rather it will continue blinking, so make sure press enter after you typed in correct password.**
    - Once you give your correct password and are logged in, the terminal will show this code :
        ```
        # Now on remote server
        Last login: Sun Jan  2 14:03:05 2022 from 107-217-10-235.lightspeed.sndgca.sbcglobal.net
        quota: No filesystem specified.
        Hello cs15lsp23zz, you are currently logged into ieng6-203.ucsd.edu
        
        You are using 0% CPU on this system
        
        Cluster Status 
        Hostname     Time    #Users  Load  Averages  
        ieng6-201   23:25:01   0  0.08,  0.17,  0.11
        ieng6-202   23:25:01   1  0.09,  0.15,  0.11
        ieng6-203   23:25:01   1  0.08,  0.15,  0.11
        
        Sun Jan 02, 2022 11:28pm - Prepping cs15lsp23
        ```
    - Now your terminal is connected to a computer in the CSE basement, and any commands you run will run on that computer! 

## Step Three : Trying Some Commands : 
Now you are on a computer in the CSE basement, try running some commands such as `cd`,`ls`,`pwd`,`mkdir`,and `cp` a few times both on your computer and on the remote computer.\
Here are some specific useful commands to try : \
- `cd ~ `\
- `cd`\
- `ls -lat`\
- `ls -a`\

Hint : To log out of the remote server in your terminal, you can use either one of the following method : \
- Ctrl + D \
- Run the command `exit` in the terminal
