# Lab Report 5 Week 10
The following tests were made by running the `bash script.sh > results.txt` command in **ieng6** on both the markdown-parse implementation from lab 9 and from my lab group. I then used the command `diff markdown-parse-lab9/results.txt markdown-parse/results.txt` in order to compare the results files of both the lab 9's markdown-parse and my group's markdown-parse. 

## Test 1: 194.md
---
The following image shows the contents of the 194.md file. 
![labrep5_test1contents](https://user-images.githubusercontent.com/97699019/157831596-b674c61a-c8e7-43a3-92dd-68249eac075a.png)

<br>
The following image contains the comparison between my group's implementation and the professor's implementation. The top output represents the professor's while the bottom output is my group's.

![labrep5_test1](https://user-images.githubusercontent.com/97699019/157831580-6f7e87a2-b4db-4d7c-9967-c45aaeb54ae0.png)

<br>

Professor's Output: `[url]`

My Output: `[]`

The image below shows the expected result for the 194.md file. As we can observe from CommonMark, the output is not the same for either implementation of markdown-parse.
![labrep5_expected194](https://user-images.githubusercontent.com/97699019/157850142-b16726ad-6565-4c65-88b0-c53a6b6af834.png)

![labrep5_wherecodefix194](https://user-images.githubusercontent.com/97699019/157856080-5cf853b0-ebae-466c-a0b7-3786bf28fb60.png)



## Test 2: 32.md
---
The following image shows the contents of the 32.md file.
![labrep5_test2contents](https://user-images.githubusercontent.com/97699019/157831594-4b2f6ea9-43b6-4abd-92b0-551e399e462f.png)

<br>
The following image contains the comparison between my group's implementation and the professor's implementation. The top output represents the professor's while the bottom output is my group's.

![labrep5_test2](https://user-images.githubusercontent.com/97699019/157831598-9f917a70-1f79-4128-9753-5806c113dc94.png)

<br>

Professor's Output: `[]`

My Output: `[/f&ouml;&ouml; "f&ouml;&ouml;"]`

The image below shows the expected result for the 32.md file. As we can observe, both implementations are wrong as they do not match the CommonMark output.

![labrep5_expected32](https://user-images.githubusercontent.com/97699019/157850141-2d495f37-85cf-4dfe-9952-9f02d1125610.png)

Looking at my group's implementation I believe that we need to include another if statement after line 27 in order to check for characters after an `(` that do not follow the format for a link (i.e https://....). We can than write code that prints what is between the `[]`.

![labrep5_wherecodefix32](https://user-images.githubusercontent.com/97699019/157854563-7fc95e19-7e1b-491b-9a35-130549fcd554.png)
