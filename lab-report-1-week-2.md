# Week 2 Lab Reprt
## Guide for logging into a course-specific account on _ieng6_

Note: This guide is intended for Windows computers.

- Installing VScode
- Remotely Connecting
- Trying Some Commands
- Moving Files with scp
- Setting an SSH Key
- Optimizing Remote Running


---
# Installing Visual Studio Code

Head to the [__Visual Studio Code__](https://code.visualstudio.com/) website to download and install it. Follow the link and be sure not to mistakenly install _Microsoft Visual Studio_ (without _"Code"_ at the end of the name) instead.

We want the blue one
![Visual Studio vs Visual Studio Code](Visual-Studio-vs-Visual-Studio-Code.png)

The download page
![Visual Studio Code Website](VS-Code-Website.jpg)

It should look like something this after installation (dark theme enabled)
![Visual Studio Code](VS-Code-Launch.png)


---
# Remotely Connecting

### Install the program [__OpenSSh__](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse).
Learn more about SSH (Secure Shell Protocol) on [Wikipedia](https://en.wikipedia.org/wiki/Secure_Shell).

### Find your course-specific account with the [UCSD Account Lookup Tool](https://sdacs.ucsd.edu/~icc/index.php).

### Return to Visual Studio Code and open a terminal. Input the following command (with '%f' replaced by the quarter, year, and account):

> `ssh cs15l%f@ieng6.ucsd.edu`

An example account could be cs15lsp22zz@ieng6.ucsd.edu with 'sp' for Spring quarter, '22' for the year 2022, and 'zz' for the account name. Quarter abbreviations are as follows: Fall = fa, Winter = wi, Spring = sp, Summer = su.

- If you are connecting for the first time, you will see the following prompt to which you should respond with yes:

````
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.

RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.

Are you sure you want to continue connecting (yes/no/[fingerprint])?
````

- Input your password and your computer (the client) should now be connected to the server

![remotely connecting](remotely-connecting.png)

Additonal instructions on connecting to a remote host available on the [VS Code Website](https://code.visualstudio.com/docs/remote/ssh#_connect-to-a-remote-host).




---
# Trying Some Commands



---
# Moving Files with SCP




---
# Setting an SSH Key
## Extra steps for Windows devices:
![Image](CS-15L_lab-wk1_keygen-powershell(1).jpg)

![Image](CS-15L_lab-wk1_keygen-powershell(2).jpg)




---
# Optimizing Remote Running

---
# Useful Links:
[Lab 1 Instructions Writeup](https://docs.google.com/document/d/1ZJsxrCRiXRbgBpAxhTRwIIqs2-xILh4EZEXfhyADS7I/edit) (this assignment)

[CSE 15L Lecture Slides week 1](https://docs.google.com/presentation/d/1M1usJWoXlajH29ONzpQ7L2BxeHMdL3C7sMUSBtogpOw/edit#slide=id.g9aaf8b0d81_0_25)
(Spring 2022 with Professor Gerald Soosai Raj)

Lab Group Google Docs with TA Jessica Lam (need permission to access):

[Lab Week 1](https://docs.google.com/document/d/1bWz30m_V0ENEkdCKICzX2L37mdhOCcbEqrSbeqsJ2QA/edit#heading=h.s8u88f6kqofr) (2022.03.31); 
[Lab Week 2](https://docs.google.com/document/d/1EMxWD-WkNZeto2HrgJhavFGu7xCwQafZ3rzX2057TDY/edit#) (2022.04.07)
