# Lab Report 2 Week 4

<br>

## Code Change 1
---

![code1](https://user-images.githubusercontent.com/97699019/151641886-1f5306b1-ce78-4cef-9c6f-d7c2c7f7c189.png)
Link to *failure inducing input* file [here](https://github.com/rpaquia/markdown-parse/blob/main/test-file2.md)

Output of running test-file2.md
![code1fail](https://user-images.githubusercontent.com/97699019/151642353-65c469f2-262c-42a0-86b1-bce1656e6e1e.png)

The symptom here was an OutOfMemoryError caused by a bug that occurs when the while loop would iterate past a string and read characters not contained in brackets or parenthsis. The failure inducing input created in test-file.md reveals this bug in MarkdownParse by including a bare URL that is not written in markdown syntax. The "www.Google.com" URL is not surrounded by anything which allows the while loop to run on an infinite loop, creating our symptom. 
<br>


---
<br>

## Code Change 2
---

![code2](https://user-images.githubusercontent.com/97699019/151643768-a736fc36-ecb6-4f36-8558-8beaab51eb8e.png)
Link to *failure inducing input* file [here](https://github.com/rpaquia/markdown-parse/blob/main/test-file3.md)

Output of running test-file3.md
![code2fail](https://user-images.githubusercontent.com/97699019/151643771-192c1f6c-1b89-4c61-97f2-a80892399de6.png)

The symptom here was an IndexOutOfBoundsException caused by a bug that occurs when the while loop would read through the characters within brackets but could not find parenthesis after the brackets to read a URL. The failure inducing input from testfile3.md creates the beginnings of a markdown formatted link however does not include a parenthesis enclosed URL that must come after the link's markdown declaration. Since there are no "()" after the brackets, the while loop returns "-1" for the current index causing our IndexOutofBoundsException symptom.
<br>



---
<br>

## Code Change 3
---

![code3](https://user-images.githubusercontent.com/97699019/151645038-a030c193-c49c-4e9c-b6e4-502c2a6e03bb.png)

Link to *failure inducing input* file [here](https://github.com/rpaquia/markdown-parse/blob/main/test-file8.md)

Output of running test-file8.md
![code3fail](https://user-images.githubusercontent.com/97699019/151644972-4ac14e92-d351-4720-ba32-b5c71809a033.png)

The symptom here was an OutofMemoryError caused by a bug that occurred when the code catches an extra bracket when reading through a markdown formatted image or link. The failure inducing input from file-test8.md tests how the MarkdownParse file reacts when a markdown link is properly written and inputted, but has an extra "[" after the link. The while loop inside MarkdownParse catches this bracket and tries to read characters until finding the "]", which is not there, allowing the loop to continually run, unable to print an output, causing our symptom.

---
<br>



