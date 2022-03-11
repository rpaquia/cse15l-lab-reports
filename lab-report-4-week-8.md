# Lab Report 4 Week 8
<br>
"markdown-parse" Repository Links:
<br>

[Ryan Paquia's Repository](https://github.com/rpaquia/markdown-parse)
<br>

[Other Lab Group's Repository](https://github.com/christopherthomason/markdown-parse)

---
## Snippet 1

<br>

**What should be produced (Using VScdoe Preview):**
![snip1_myimpprev](https://user-images.githubusercontent.com/97699019/155816432-99162584-767e-45b4-811f-9a9a85eabe7b.png)

<br>

**Test for snippet 1**
![snip1_myimptest](https://user-images.githubusercontent.com/97699019/155819935-57862501-5e19-4808-87f5-94487f7b2773.png)

<br>

**Output (My Implementation) - FAIL**
![snip1_myimperror](https://user-images.githubusercontent.com/97699019/155818672-0583553e-6743-44cf-9792-39d59e2dc32d.png)

<br>


**Output (Other Implementation) - FAIL**
![snip1_otherimperror](https://i.gyazo.com/b3af76aedfa2f7ad9441d0d0ebbc23e8.png)

<br>

**Question 1**:
For cases that use inline code with backticks, one possible work around is to implement code that detects the backticks and if they are detected, check if they are preceded by a closing bracket or parenthesis. Such a change should require less than 10 lines of code.

---
## Snippet 2

<br>

**What should be produced (Using VScdoe Preview):**
![snip2_myimpprev](https://i.gyazo.com/820500ba1ccca12857c97c637daa4882.png)

<br>

**Test for snippet 2**
![snip2_myimptest](https://i.gyazo.com/8de2625e47de9ac49996dc086b44fcd1.png)

**Output (My Implementation) - FAIL**
![snip2_myimperror](https://user-images.githubusercontent.com/97699019/155818687-f15a8c25-a46c-41c1-a549-e45848d2505a.png)

**Output (Other Implementation) - FAIL**
![snip2_otherimperror](https://i.gyazo.com/992d706979f09df2d6e8bcc351c22b9d.png)

<br>

**Question 2**: For cases with nested parentheses, brackets, and escaped brackets we can check a `[` for its matching `]` by searching for the right-most `]` and to ignore any nested or escaped brackets. The same can be done when we have nested parenthesis. I imagine this would take >10 lines using a while loop that could loop through these cases so that we can continually check for the right most `]` and/or `)` and break once we have found the matching `]` and/or `)`.

---
## Snippet 3

<br>

**What should be produced (Using VScode Preview):**
![snip3_myimpprev](https://i.gyazo.com/ee9f95a4f51de2626b529d34e9d0e159.png)

**Test for snippet 3**
![snip3_myimptest](https://i.gyazo.com/44dfc4609d03c18705dac9524fb349cb.png)

**Output (My Implementation) - FAIL**
![snip3_myimperror](https://user-images.githubusercontent.com/97699019/155818695-c0a15b67-5b08-434d-8eb1-4c29ed908480.png)


**Output (Other Implementation) - FAIL**
![snip3_otherimperror](https://i.gyazo.com/5f6ca24ba861ebf143927b807774a9cf.png)

<br>

**Question 3**: A an idea for a code change could be that as we iterate through the strings of the markdown file we check for when the line ends and once the end is reached the code continues on the next, checking for when the string picks back up and continues reading in characters from there. A while loop could be used here to constantly check for newlines in brackets and parentheses. This code may take longer than 10 lines because we also have to make MarkdownParse correctly identify and match closing brackets or parenthesis that may be on a new line.

---

