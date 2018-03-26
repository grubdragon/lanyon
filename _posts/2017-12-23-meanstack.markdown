---
layout: post
title:  "A wild couple of weeks on MEAN Stack"
tags: [web, development, mean, game]
assetsdir: /assets/meanstack
---

Hey folks!

Its been a while since my last post. Just wanted to write something down, just for the heck of it. It has been a fun winter up until now, let's hope this continues to be the case. Moving on.

I had taken up coordinatorship in Mood Indigo 2k17 this summer, under the Web Department, (although I really don't like web dev, makes you do tonnes of work without any scope for innovation, I'll post about this debate soon :P) Creatives. The task at hand was to make a game for peeps to play on the weekend before MI2k17.

We were initially thinking about an RPG style thing, but since "playable by all" was the goal, we settled on a somewhat popular format, that of a cryptic puzzle, aka Enigma.

### Game format
So for those who didn't play, here's a quick gist of the game. The game was themed around Harry Potter. The game had multiple levels, 17 to be exact, each with its own clue and storyline; the clue being a single image and the storyline being an excerpt from the books. Each level had one and only one answer. The excerpt had a few words highlighted in one of red or blue, having a special meaning with respect to the answer. Each answer is hard to crack, and needs a lot of creative thinking.

## Development
So the game was made using MEAN stack, a software bundle comprising **M**ongoDB(a popular NoSQL database), **E**xpress.js(framework for Node.js to build APIs and stuff), **A**ngularJS(or Angular) (used for frontend: consuming APIs and routing) and **N**ode.js (backend runtime environment).

### MongoDB: to hate or not to hate
This is basically why I wrote this article. RANT STARTS.
MongoDB is a very well *marketed* NoSQL database. MongoDB follows Databases > Collections > Documents; for any app you make, generally you make a database, each database with multiple collections for a particular purpose. For example, enigma used a database named treasure, with two collections: 'questions' and 'users'. It stores data in JSON documents, meaning fields can vary from document to document and data structure is mutable. This looks all well and good when worded like this:
<div class="message">
  MongoDB is a document database with the scalability and flexibility that you want with the querying and indexing that you need
</div>
What they term as flexibility, might not be a great thing for you. MongoDB doesn't have data checks, and it requires you(the developer) to maintain it by yourself, on backend. This is my biggest turn off as a developer. I'd rather work with a structured query language.

Since I did not work with the server side, I don't know server-side pains. But from what I've read; MongoDB takes too much space, and on every database update, the redundant data is not flushed till server is restarted or removed manually. Although MongoDB markets its speed 
<div class="message">
  Scale horizontally to deliver incredible performance at massive scale: millions of ops/sec, 100s of billions of documents, petabytes of data.
</div>
it is achievable only if you have the right indexes. 

But its not fair to give MongoDB so much flak, it has its own advantages. MongoDB is scalable horizontally being a NoSQL database. Server calls are asynchronous and quick if you don't query with too many filters.

The 'flexibility' in the data model, which I so very well hate, can come in handy to certain use cases. Also, with a very good documentation and pretty great query methods, MongoDB can be extremely good, and commands on it can simply be executed by adding them to a ```code.js``` and running ```mongo code.js```. Personally, I saw the exporting and importing slightly painful, given that I could only export collections and not the database in itself. Also, with tools like [Robo 3T](https://robomongo.org/){:target="_blank"}, managing databases has become much easier, without needing to fight through many mongo commands. That and seamless integration into MEAN stack, really gives MongoDB an edge.

You can find a critical, to-the-point description of the above and more [here](https://dzone.com/articles/mongodb-the-good-the-bad-and-the-ugly){:target="_blank"}.

Verdict: BE A MAN AND GET A REAL DATABASE YOU LOUSY BOYO
![Act like a goddamn man]({{page.assetsdir}}/act-like-a-man.gif)
<hr>
### Angular(JS): King of all things frontend
AngularJS. Ahhhh. I remember my days of struggle with it. Tried so much with Angular, but never found a decent tutorial. Legend has it that some souls are still looking for an Angular tutorial. To be honest, I directly looked at code, before even looking at a tutorial. NOT INTUITIVE, I repeat NOT INTUITIVE.
Anyway, from what I understand, Angular is used for SPAs or Single Page Applications. This is basically for better user experience, given that the page doesn't reload everytime. It is one of the more comprehensive client-side solutions.

<center><i class="fa fa-circle-o-notch fa-spin" style="font-size:24px"></i></center>
