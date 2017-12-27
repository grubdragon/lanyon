---
layout: post
title:  "A (Simple) Subtitler in Python"
date:   2017-09-30 15:20:00 +0530
categories: [python, tutorial, rattlesnake]
---
Being a part of the Web and Coding Club (WnCC), has its perks, and you can often find yourself doing some randomly productve things for it.

This blog post is in tandem with WnCC's  [rattlesnake][rattlesnake], a workshop introducing non/inexperienced coders to python as a tool for automating what they want.

_"Instead of the traditional approach where beginners are made to learn language elements first without making anything substantial, we try to build something in every problem."_
<hr>
  
### ENOUGH ABOUT THAT! LET'S GET DOWN TO WORK!
*Objective:* To make a python program which can take an srt file and play it according to the timestamps in the file.

*Assumption:* We will use a lyrics srt file, i.e. none of the subtitles will overlap in our case

Let's start! Open a blank `subs-easy.py` file for yourself. Let's put our task in perspective: we need to: 1) Open/decode an srt file 2) Implement logic to store delays between subs and 3) Display it at the appropriate time. Might seem a bit scary in the start, but don't worry we'll deal with it!  

So, first things first, 'How to open an srt file in python?' Google it. Easy, right?
Well, the first result is `pysrt`. It does all the hard work for us, so let's use it! (essential part of programming is "Don't reinvent the wheel" which I often inaccurately subtitute as "Why the hell are you working so hard?")  

Scroll below to see the installation part. Plain and simple(If you didn't understand it, you should look up the [Beginner's Guide to Python][Beginner's Guide to Python] on the [WnCC wiki][WnCC wiki]).  

Scroll further and lookup usage. Hmmm.
{% highlight python %}
subs = pysrt.open('some/file.srt')
total_subs = len(subs)
first_sub = subs[0]
print first_sub.text
#=> prints 'Hello World !' to STDOUT.
print first_sub.start.seconds
#=> prints '20' to STDOUT.
print first_sub.end.minutes
#=> prints '5' to STDOUT.
{% endhighlight %}

> Self-note: Looking through the entire usage, if I ever make a python video player, I might give this lib a whirl.

I guess we've solved part 1! Pysrt easily parses the srt file! Time to add code! There isn't much to add here though; just some import statements, a line to open the subtitles. Now for part 2: <b>Implementing logic to..ummm...</b>

Yes, so, what I mean by part 2 is that we'd need the difference in times between consecutive subtitles. Also, we'd need the amount of time a subtitle should be displayed. So how can we approach the problem? Lets start off with a new function, that can scale your time in hours, minutes, seconds and milliseconds to a common metric. Lets say, to seconds.  

So make a new function `scale_to_seconds` which provides the above conversion.  
Cycling through each subtitle, append to two lists, the start and end time of each subtitle.(obviously, make global variables for ease of access)

Now that we have this data, our next step is to take the delays I've been talking about, while moving through the subtitles. You could use two variables,

`delayBefore = scale_to_seconds(subs[i].start)-scale_to_seconds(subs[i-1].end)` 
`displayFor = scale_to_seconds(subs[i].end)-scale_to_seconds(subs[i].start)`

And make lists out of it.
> Stupid Pro tip: You don't need four lists, you could just use the two lists for delays, the first two are redundant

Hey, but wait! You didn't realize something! For i=0, `delayBefore` tries to access subs[-1], which is an error! Figure this one out yourself, okay?

You know what? We're already kinda done, only thing left is display of lyrics! Time to add some code, everything that's relevant to storage and processing of delays!

So now that we have all the data we need, we simply need to display stuff. Here we will be using the `time` library. Mainly we need only `time.sleep()`, which is used for pausing code execution. We can now loop through all lyrics, access each `delayBefore` and start by `time.sleep()`ing for that much time. Then we print the current lyric and `time.sleep()` for `displayFor` time. Optionally, clear the previous output before displaying the curret lyric, could give you the relevant subtitles for the current time.

### And we are done!

Thanks for reading! Be sure to drop by once in a while, you might learn a thing or two. You could comment in the below section, start a discussion and/or definitely tell me my mistakes.[Comment section in progress, till then you can contact me over 

If you want to refer to a typed out solution to the problem, please look for `subs_easy.py` in [this][random-python-scripts] repo.

[rattlesnake]: http://wncc-iitb.org/wiki/index.php/Rattlesnake
[WnCC wiki]:   http://wncc-iitb.org/wiki/index.php
[Beginner's Guide to Python]: http://wncc-iitb.org/wiki/index.php/Python_for_Beginners
[random-python-scripts]: https://github.com/grubdragon/Random-Python-Scripts
