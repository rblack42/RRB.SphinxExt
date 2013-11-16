Sphinx Extensions for Literate Programming
##########################################

..  include::   /references.inc

I my teaching activities, I document a lot of programming code. I use Sphinx_
to create my lecture materials, and often include fragments of code in those
documents. 

In the past, I have typed in code snippets into a ``code-block``. The
code looks nice, but often has errors because it has not been tested. What I
really want to do with my lecture notes is show code fragments that actually
can be run, and capture the output from those fragments in my notes as well.
That would eliminate the embarassment of spotting mistakes in the code and
explaining what the code should really look like in class!

Source code control
*******************

All programmers should use a source code control system. Currently the best of the ones available is probably Git_, written by Linus Torvalds to help him manage the Linux Kernel development. I have used Git_ for several years, but never really explored all of its capabilities. ONly recently have I started to use branching and tags to mark interesting points in the development of my code. In one of my many creative thinking sessions I conduct while stuck in traffic on my way to work, it occurred to me that I could use Git_ tags to mark points in the development of a rogram I want to include in my lecture notes, then have Sphinx run Git_ to revert the code to that tag point, and include code that existed at that point in time. This is cool! It will give me a way to move back and forth in time to explore the code as it was, not just as it is at the present time!

Baby Steps
==========

I encourage my students to write their code using a technique I call "Baby
Steps". This is nothing new. What I want them to do is to compile and run their
code often, not just occasionally after a marathon coding session. The idea is
to focus attention on one small chunk of code at a time, and test it as soon as
possible. I often walk up to a student and ask then to run what they have at
that moment. Sure, it may fail to compile, due to typing mistakes, or
incomplete code. But, they will disciver those errors right away and be able to
fix them on the spot. The error messages they experience will be related to
what they are typing right now, not something they created hours ago.

What has been missing in this concept was a way to demonstrate this concept in
my lecture notes. The idea behind this extension is to use Git_ to tag points
in the development of my program example code, then restore the code to
thosetag points and include the code as it existed at that point. In this way,
Git_ is managing my program examples, and letting me show how to build that
code using my "Baby Step" approach!. I am betting this will help show them a
better way to code!

Git tags
********

Git_ supports the notion of a branch, as do all :term:`source code control
systems`. It also supports the notion of a tag, which is just a way of placing
a label on a version of the project code at some point in time. In the
development of a big program, these tags might just be used a reference points.
They are similar to branch points, but there is no plan to begin a new track of
code development at this point. WIth a branch, we do plan on creating a
completely different version of the program for some purpose.

Tags are markers at a point in time. For my purposes, I do not need to mark
points in the development of the entire project, but I do want to mark points
in the development of an example code fragment. My Git_ repository will hold
many code examples, each of which needs to be tagged to show how it was
developed using my "baby STep" procedure. WHat I need to do is to create tag
names that I can create any time I wish to return to a fragment and continue
development. This will happen whenever needed, not in some time linear fashion.

Tag names
=========

A simple naming scheme is just a fragment name followed by a tag number. For my
purposes, the names we use need to be ordered so they can be shown to the
student in that order. The numbering scheme should work, but we might need to
consider adding steps between two existing tags as notes evolve. The naming
scheme should support doing this. If we can extract a complete list of tags for
any particular code example, and order those tags, this should work. Getting a
list of tags should be pretty simple. Ordering that list needs to be
considered. A simple alphabetic sort might work, but the numbers will sort in
an unexpected way. THis is a solvable problem, but needs to be part of the
development.

Setting up a project
********************

As an example of using this system, let's use the current project as an
example. I have a project configured the same way I organize a course. The
Sphinx configuration is set, and a Python_ Fabric_ ``fabfile.py`` has been
created to create the HTML files I will eventually post to my web server. WHat
remains to do is to set up the Git_ repository for this project, and publish
that project on a Git_ capable server. FOr this project, (and for most of my
courses), I will use GitHub_.





