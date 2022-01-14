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

## Step 2- Remotely Connecting
* For Windows users, you must first install the program [OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) (Don't do this if you are not on Windows). Afterwards, find your course-specific account [here](https://sdacs.ucsd.edu/~icc/index.php).
* Open VSCode and open a terminal (Ctrl or Command + (tilde symbol), or use the Terminal → New Terminal menu option). Type the following command into the terminal but replace the "zz" with the letters in your course-specific account. Follow the intructions that the terminal sends to you. If you enter `$ ssh cs15lwi22zz@ieng6.ucsd.edu`  and are asked a yes/no question type `yes` into the terminal.
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
* Your terminal should look similar to the image below. 

<br>

![remotely_connect](https://user-images.githubusercontent.com/97699019/149443927-02d0419a-86fa-4d6d-9689-eb0e194a2548.png)\

<br>

## Step 3 - Trying Some Commands
* Try running the following commands on *your* computer (__client__) and then try them on the *remote* computer (**ieng6**).

`cd`

`cd ~`

`ls`

`ls -lat`

`ls-a`

`pwd`

`mkdir`

`ls <directory>` where `<directory>` is `/home/linux/ieng6/cs15lwi22/cs15lwi22abc`, where the `abc` is one of the other group members’ username

`cp /home/linux/ieng6/cs15lwi22/public/hello.txt ~/`

`cat /home/linux/ieng6/cs15lwi22/public/hello.txt`

* In order to get of the remote server you can type `Ctrl-D` or enter `exit` into the terminal. Below is an example of these commands in practice. 

<br>

![commands](https://user-images.githubusercontent.com/97699019/149457188-95802f41-2bad-4dee-854f-649017a15013.png)

<br>

## Step 4 - Moving Files with scp
* Create a file on your computer called `WhereAmi.java` and put the following code into it:
```
class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
```
* Compile the file using `javac` and run it using `java`. Then, in the VSCode terminal type in the following command:

```
scp WhereAmI.java cs15lwi22zz@ieng6.ucsd.edu:~/
```
* You will be prompted to enter a password. After entering one, log back into ieng6 using `ssh cs15lwi22zz@ieng6.ucsd.edu` and enter `ls` into the terminal. You should see that your java file is in your home directory of your course-specific account. (Look at bottom of screenshot for reference)

![scpWhereAmI](https://user-images.githubusercontent.com/97699019/149462537-2d7fb683-4b91-4366-b759-2867b4e30bad.png)



