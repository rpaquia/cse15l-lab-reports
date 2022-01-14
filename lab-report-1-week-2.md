# Lab Report 1 Week 2

## How to: Logging Into a Course Specific Account on ieng6
---

## Step 1 - Install VSCode
* Visit the VSCode website at https://code.visualstudio.com/download and follow the instructions for installing VSCode. 
* Make sure that you select the verion of VSCode that matches the operating system you are using. Refer to the images below so you know what this process should look like.
<br>
<br>

![vscodepage](https://user-images.githubusercontent.com/97699019/149440820-ae26fde4-44d7-4b84-bc45-c93a48ea71e7.png)
![vscode_main](https://user-images.githubusercontent.com/97699019/149440833-24f9634b-915d-4312-9071-fe79fb9ed0bd.png)

<br>
<br>

## Step 2- Remotely Connecting
* For Windows users, you must first install the program [OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) (Don't do this if you are not on Windows). Afterwards, find your course-specific account [here](https://sdacs.ucsd.edu/~icc/index.php).
* Open VSCode and open a terminal (Ctrl or Command + `, or use the Terminal → New Terminal menu option). Type the following command into the terminal but replace the "zz" with the letters in your course-specific account and do not include the "$".
```
$ ssh cs15lwi22zz@ieng6.ucsd.edu
```
Example:
```
⤇ ssh cs15lwi22zz@ieng6.ucsd.edu
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
```
![remotely_connect](https://user-images.githubusercontent.com/97699019/149443927-02d0419a-86fa-4d6d-9689-eb0e194a2548.png)



