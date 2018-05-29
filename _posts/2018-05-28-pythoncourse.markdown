---
layout: post
title:  "A Course in Python"
tags: [python, development, tutorial]
---

This blog post contains all the information for the Python Course as part of TSS by UGAC - IIT Bombay. (Instructor for Python(2018))

## Transcript of Sent Emails
<div class="message">
  Bring your laptops along with you with python installed in it. You can find the instructions to install python <a href="http://docs.python-guide.org/en/latest/starting/installation/">here</a>
</div>

<div class="message">
Greetings!
Here's something that will interest you. An awesome book on python shared by our instructor. The link to it is as follows : <a href="https://automatetheboringstuff.com/">Automate the Boring Stuff</a>
Also for the Mac users having trouble opening IDLE here is something that might help you out:  <a href="https://docs.python.org/3/using/mac.html">MacPython</a>
</div>

<div class="message">
  A brilliant post to go through to understand the basics: <a href="https://medium.freecodecamp.org/learning-python-from-zero-to-hero-120ea540b567">Learning Python: From Zero to Hero</a>
</div>

<div class="message">
Here is the link to the material used during the class:
<a href="https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/">MIT - 6.0001 - Introduction to Computer Science and Programming in Python</a>
</div>

## Assignments
Herein lie the assignments I have given out to the course takers.

### Assignment 1
Write a cryptography program. It should have the following functions:
 - caesar(s, shift, enc): takes a string and caesar-shifts the string by integer "shift"
 - rot13(s, enc): takes a string and uses rot13 cipher on it
 - coltrans(s, key, enc): takes two strings, s and key(where key is space separated numbers of columns) and applies Columnar Transposition. Depending on the number of numbers in key, the behavior may differ i.e. using 5 numbers means you need to use 5 columns 
 - skip(s, skip, enc): takes a string and applies the skip cipher using the integer skip.

'enc' is a boolean value. If you pass enc as True, it should encode, and as False it should decode.
 
 Some reference information that might help you:
* [Caesar Shift](http://rumkin.com/tools/cipher/caesar.php)
* [ROT13](http://rumkin.com/tools/cipher/rot13.php)
* [Columnar Transposition](http://rumkin.com/tools/cipher/coltrans.php)
* [Caesar Shift](http://rumkin.com/tools/cipher/caesar.php)
