---
title: how to comment your code?
date: 2015-03-10
categories: coding
---

Have you ever seen the following:

```
// To restart
void restart();
```

If yes, you should fight against it. This type of comment does not add any value, it is redundancy information. By writing them, the amount of code to read is increased. Have this all over in your code, and it will be like reading a book in the darkness. You will need to make an effort to sort out what information is useful, and which one is not.
If the software department you work in uses tools such as [doxygen][1] with metrics about documentation coverage, then there is a good chance that you have these types of comments all over.

Now, let's look to a different kind of comment:

```
timer = 1000; // unit 1ms = 1sec
```

At first, you could assume that this is right, but what about a better naming and no comment:

```
timerInMilliseconds = 1000;
```

Regarding comments, after using different programming languages in different contexts for some years, I do largely prefer to read code which is self-explaining.

> Read the comments to understand the code is like opening a dictionary to understand a discussion.

Of course there are some exceptions, like implementation of complex algorithms. But in most cases, you can achieve no comments by putting pressure on:

- naming
- refactoring
- examples
- tests

Stress this through code reviews, and you will gain one of the criteria to have a more maintainable solution.

Two additional great sources about style and commenting:

[Linux Kernel Coding Style][2]

*Chapter 5: Commenting*

*Comments are good, but there is also a danger of over-commenting. NEVER try to explain HOW your code works in a comment: it's much better to write the code so that the working is obvious, and it's a waste of time to explain badly written code.*

*Generally, you want your comments to tell WHAT your code does, not HOW. Also, try to avoid putting comments inside a function body: if the function is so complex that you need to separately comment parts of it, you should probably go back to chapter 4 for a while. You can make small comments to note or warn about something particularly clever (or ugly), but try to avoid excess. Instead, put the comments at the head of the function, telling people what it does, and possibly WHY it does it.*

[Google C++ Style Guide][3]

*Though a pain to write, comments are absolutely vital to keeping our code readable. The following rules describe what you should comment and where. But remember: while comments are very important, the best code is self-documenting. Giving sensible names to types and variables is much better than using obscure names that you must then explain through comments.*

*When writing your comments, write for your audience: the next contributor who will need to understand your code. Be generous — the next one may be you!*

[1]: http://www.stack.nl/~dimitri/doxygen/
[2]: https://www.kernel.org/doc/Documentation/CodingStyle
[3]: http://google-styleguide.googlecode.com/svn/trunk/cppguide.html#Comments