# Part 1: Committing to the story

## Learning outcomes

- Learn to define what a git repository is
- Learn to define what a git commit it
- Identify what a git hash is
- Learn how to view the git log

## Lesson

Throughout this and the next lessons we will be using git in a creative retelling of the Back To The Future story.

For the uninitiated, in the story of Back To The Future, the protagonist (Marty McFly) finds himself accidentally transported from 1985 to 1955 and triggers what is known as the "Grandfather Paradox". A type of temporal complication known as an "Infinite Regression Paradox". A paradox is a contradictory statement that appears to remain true, despite its contradictions.

An example might be: "That sucks worse than a broken vacuum cleaner", well a broken vacuum cleaner doesn't suck, so as a vacuum it sucks, which means it doesn't suck, which means it sucks, etc

The grandfather paradox is similar: You go back in time to kill your grandfather, so you were never born, and if you were never born, you never went back and so your grandfather is alive, which means you were born, which means you go back, which means you were etc.

Before we get to the end of Act I, however, we must fill in some details (and do things with git), so it's time to get started.

    $ mkdir bttf
    $ cd bttf
    $ git init
    
Hopefully the concept of creating and entering a directory is not new to you, as I do not have the scope to explain `mkdir` and `cd`. What is important to know is the `git init` command.

This simple command sets up the directory you are in as a git `repository`, a `repository` is a term to refer to a project managed by git. It does this by creating a directory called `.git` in the directory you are in. It's called `.git` because in Linux, Unix, MacOS, and most other computer systems, this is how a directory is hidden (Windows is different and is, to my knowledge, the only system where hiding files and folders doesn't work the same way) and since git was developed by the guy who developed Linux, to help him develop Linux, it makes sense that gits design and features work well with Linux and related systems.

This directory is a database of changes to your project. It's important to note that git is a change management system, it tracks changes, but it's important to note that it's just a piece of software and doesn't have any awareness of what the nature of the changes are and can't perform miracles, it still often requires humans to make the ultimate choice when things end up in a state of conflict.

## Terms

- [repository](#)
- [commit](#)
- [hash](#)

## Resources

- [Time Travel](https://plato.stanford.edu/entries/time-travel/)
- [git init reference](https://git-scm.com/docs/git-init)
