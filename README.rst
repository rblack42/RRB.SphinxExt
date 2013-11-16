Sphinx extensions for teaching Computer Science
###############################################

..  include::   /references.inc

This project was established to manage Sphinx extensions I have created for use
in my lecture materials at |ACC|_. There are several extensions present here, each has
found its way into my lectures at some point.

The best way to explore these extensions is to clone this project as follows:

..  code-block:: text

    git clone https://github.com/rblack42/RRB.sphinx
   
Then, follow these instructions to set things up:

..  note::

   I do my software development on a MacBook Pro. The material here assumes you
   are working on a Linux/Mac system. If you are using a PC, several of the
   commands will be different. I will note where that happens in these notes.


Project setup
*************

This project needs a virtualenv_ with Sphinx and a few additional tools
installed. The repo you just cloned does not have this set up, so you need to
at least have virtualenv_ installed up on your system to proceed. Once that has been
done, do this:

..  code-block:: text

    cd <project folder>
    virtualenv _venv

I set up the same virtual environment directory in all of my project
directories. I have added a line in my ``.bash_profile`` file that makes it
easy to start working on a project. On a Mac/Linux system edit (or create) the
``.bash_profile`` file in your home directory and add this line:


..  code-block:: text

    alias workon='. _venv/bin/activate'

..  note::

    you will need to start a new Terminal session to activate this alias, or do this:

    ..  code-block:: text

        source ~/.bash_profile

Now, you can activate a project in a :program:`terminal` session by doing this:

..  code-block:: text

    workon

Your prompt should change to someething like this:

..  code-block:: text

    (_venv)MacBookPro2:SphinxGit rblack$ 

The ``(_venv)`` indicates that the virtualenv_ is active and you are using an
isolated  Python_ interpreter and installed tools.


Installing dependencies
-----------------------

Once we have an isolated project environment to work on, do this:

..  code-block:: text

    pip install -r requirements.txt

This will install all of the dependencies needed by this project. Once this
step is completed, you are ready to proceed.



