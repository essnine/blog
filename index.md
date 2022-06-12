## code: the basics.

### 23 Jan 2022

I’ve been writing (python) code for maybe three, four years now. Nearly all of it has been in the context of the web, i.e. backends, chatbots, API wrappers, and so on. And my first two years were spent writing bad code under initially a minimum amount of supervision, which quickly changed to zero supervision. Also, I do mean bad code. I was almost going to say that it made me miserable, but that’s not true. I wasn’t miserable because of the code, I was miserable because of circumstances under which that code was written. The code was not the cause of the misery, merely a symptom of it.

Anyway, not to digress.

Here’s my own take on writing good code while also learning to do it. Mind you, this is not the same as engineering. I might do that bit a little later. This is purely programming, for now. And it’s good code, not great code, or perfect code. That’s a more… zen problem. Perfect is the enemy of good, okay? Check out Tron: Legacy to understand what I mean. (Kidding. that’s not the source. Check out Tron: Legacy regardless though, while we’re at it.)

First of all, for the sake of your own sanity, add comments to your code. And I mean, add docstrings, add inline comments for the simpler stuff, add full docstrings for complex blocks of code, annotate refactor-pending parts with TODO tags, do it all. It’s unbelievably important way down the line when you have to maintain the code, and even more so when someone else has to maintain the code.

Secondly, names are important. While you do not want to go all the way to suffixing all your iterables with `_iterabletypename` or whatever, you’d be surprised to find out how much easier life becomes if you do so. On the other hand, there’s type annotations that’ll also work well instead of this naming thing, so pick whatever works for you. Do not, though, use the same variable name over and over in different logical blocks of your code, and do not use random character sequences or single characters for names. Pretty simple.

Moving on. You will learn new frameworks every now and then, and when it comes to learning, if you’re fresh, you’ll be tempted to use a single, massive file with all your stuff in it. This is OK! Be not afraid!

However, when you actually write your code to run, and when I say run I mean that it’ll go in use in some way whether that’s going up and serving end users or being shared by your peers as some sort of reference, separation is good. Think of it like adding abstraction.

Do you truly care which endpoint your third-party-user-data came from when you’re trying to deconstruct-comprehend-reconstruct it into your API’s designed output format? Does your JSON-object-creator method care about the contents of the hashmap it’s going to parse? (Well, it might care, which you can handle using the method’s arguments, that’s what those are for.)

You get the idea. Which then leads to a general sort of meta-pattern I’m hoping becomes apparent here as the takeaway from this post.

What does your code do? Existentially speaking, it serves users. It should be great at doing that, at any given moment as well as a function of the time spent working on it. And when you think about it, this notion of cleanliness and separation and abstraction isn’t for the benefit of the code as much as it is for the coder, since the code complexity itself is a function of time over effort x design so, that’s the formula you have to optimize for

More later.
