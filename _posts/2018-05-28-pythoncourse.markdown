---
layout: post
title:  "A Course in Python"
tags: [python, development, tutorial]
---

I was the instructor to the Python Course as part of TSS by UGAC - IIT Bombay. This blog post contains transcripts of the sent emails.

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

<div class="message">
Some resources for you:<br>
Goes from start to end, giving you a vivid taste of the language. Good for strengthening basics:<br>
<a href="https://learnpythonthehardway.org/python3/">Learn Python the Hard Way</a><br>
For an interactive learning experience (free one is good enough):<br>
<a href="https://www.codecademy.com/learn/python">Python at CodeAcademy</a><br>
To learn webscraping, making scripts and other cool stuff with Python:<br>
<a href="https://automatetheboringstuff.com/">Automate the Boring Stuff</a><br>
Webscraping only<br>
<a href="https://www.geeksforgeeks.org/implementing-web-scraping-python-beautiful-soup/">GeeksForGeeks - Webscraping Tutorial using BeautifulSoup</a><br>
How to use Jupyter Notebooks:<br>
<a href="https://unidata.github.io/online-python-training/notebook.html">How to Start and Run a Jupyter Notebook</a><br>

<a href="https://www.youtube.com/watch?v=Rc4JQWowG5I">Introduction - Jupyter Tutorial (IPython 3)</a><br>

<a href="http://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/Notebook%20Basics.html">Notebook Basics</a><br>

Numpy (Computational library of Python):<br>
<a href="https://docs.scipy.org/doc/numpy/user/quickstart.html">Numpy - Quickstart tutorial</a><br>

Also checkout Matplotlib, Pandas, Seaborn for Data Science<br>
TensorFlow, PyTorch, Sci-kit Learn, Keras for Machine Learning (Neural Networks etc.)<br>
Scipy for some Math, Science and Engineering applications<br>
Kivy, Tkinter,Qt  for GUI based stuff<br>
Pygame for Game Development<br>
OpenCV,Pillow for Image Processing<br>
Django for a Server-Side web framework<br>
eyeD3 - Working with audio files containing ID3 metadata.<br>
And many more
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
