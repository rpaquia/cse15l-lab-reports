# Lab Report 3 Week 6

<br>

## Streamlining ssh Configuration (Group Choice 1)
---

<br>

## Showing .ssh/config File
![labrep3_configfile](https://user-images.githubusercontent.com/97699019/153559635-1912ee2e-3bfd-4401-b3d5-5a14b35c1e1b.png)

Made a config file of type **File** and using Notepad for editing its contents. Alias name is set to **ieng6** and connects my course-specific account to the UCSD remote server.

---
<br>

## Logging Into Remote Server Using Alias
![labrep3_loginalias](https://user-images.githubusercontent.com/97699019/153559659-26f6aa03-2b4b-4352-a7bf-a3c9c4bfbec1.png)

Since my alias is **ieng6**, by typing **ssh ieng6** into the terminal I was able to log into the remote server without having to type in the command:
```
ssh cs15lwi22aqj@ieng6.ucsd.edu
```
---
<br>

## Copying a File to Account Using Alias

![labrep3_exfile](https://user-images.githubusercontent.com/97699019/153559652-3d427794-a043-4ae1-9b42-cc5a0c762dbe.png)
![labrep3_copyfile](https://user-images.githubusercontent.com/97699019/153559640-48ad6445-d9f6-4f70-b607-0c82cf1fc87e.png)

The top screenshot shows the file I will copy to remote server. The file will print "Hello World" when ran. I can copy the file with my alias **ieng6** by typing
```
 scp labreport3.java ieng6:~/
 ```
instead of

```
 scp WhereAmI.java cs15lwi22zz@ieng6.ucsd.edu:~/
 ```
 Looking at the bottom screenshot,  after typing **ls** in the remote server you can see my labreport3.java file has been copied into the server. The file was successfully compiled and printed "Hello World" when ran.
 
 ---



