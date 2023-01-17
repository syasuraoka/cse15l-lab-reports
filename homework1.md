# Lab homework1
## How to log into your course-specific account on `ieng6`?

## 1. Installing VSCode <br>
VSCode is a popular, free code editor with advanced features and customization options. Normally, you can install VSCode from [here](https://code.visualstudio.com/download), but sometime you've already installed VSCode for other purpose (e.g. CSE11). Once installed, you will get the screen like this.

<img src="https://raw.githubusercontent.com/syasuraoka/cse15l-lab-reports/main/スクリーンショット%202023-01-16%20午前10.20.25.png" width="35%">



## 2. Remotely Connecting <br>
You'll be able to connect to a remote computer by using VSCode terminal. <br>

First, if you are a Windows user, install `git` for Windows from [here](). Once installed, use the steps [in this post]() to set your default terminal to use the newly-installed `git bash` in VS Code. If you are a Mac user, you can skip these steps.

Then, open VSCode terminal, and type <br>
`$ ssh cs15lwi23hs@ieng6.ucsd.edu` <br>
(Note: Replace `hs` by the letters in your course specific account.)

If this is the first time you've connected to this server, you'll get the message like this.
```
⤇ ssh cs15lwi23ahs@ieng6.ucsd.edu
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
```
Type `yes` and press the enter key.

Then, you'll be asked your password. Type your password and enter, and now you're logged in. You'll terminal will be like this.

<img src="https://raw.githubusercontent.com/syasuraoka/cse15l-lab-reports/main/スクリーンショット%202023-01-16%20午後4.17.29.png" width="70%">

## 3. Trying Some Commands <br>
Try some commands in your terminal, such as
* `cd`
* `ls -a` 
* `cat /home/linux/ieng6/cs15lwi23/public/hello.txt`

You can get the screen like this. For instance, when you type `cat /home/linux/ieng6/cs15lwi23/public/hello.txt`, you'll see the contents of `hello.txt`, which is "Hello! Welcome to CSE 15L".

<img src="https://raw.githubusercontent.com/syasuraoka/cse15l-lab-reports/main/スクリーンショット%202023-01-16%20午後4.36.31.png" width="70%">



