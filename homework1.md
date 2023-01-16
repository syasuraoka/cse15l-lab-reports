# Tutorial
## How to log into your course-specific account on `ieng6`?

**Installing VSCode** <br>
VSCode is a popular, free code editor with advanced features and customization options. Normally, you can install VSCode from [here](https://code.visualstudio.com/download), but sometime you've already installed VSCode for other purpose (e.g. CSE11). Once installed, you will get this screen.
<img src="https://raw.githubusercontent.com/syasuraoka/cse15l-lab-reports/main/スクリーンショット%202023-01-16%20午前10.20.25.png" width="35%">



**Remotely Connecting** <br>
You'll be able to connect to a remote computer by using VSCode terminal. <br>
First, if you are a Windows user, install `git` for Windows from [here](). Once installed, use the steps [in this post]() to set your default terminal to use the newly-installed `git bash` in VS Code. If you are a Mac user, you can skip these steps.

Then, open VSCode terminal from Terminal → New Terminal menu option, and type <br>
`$ ssh cs15lwi23hs@ieng6.ucsd.edu` <br>
(Note: Replace `hs` by the letters in your course specific account. And remember that when we write `$`, that’s not for you to type in. It’s just a convention for how we write commands.)

If this is the first time you've connected to this server, you'll get the message like this.
```
⤇ ssh cs15lwi23hs@ieng6.ucsd.edu
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
```
Type `yes` and press the enter key.

Then, you'll be asked your password. Type your password and enter, and you'll terminal will be like this.
<img src="", >

**Trying Some Commands**




