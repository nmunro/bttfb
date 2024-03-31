# Part 1: Committing to the story

## Learning outcomes

- Learn to define what a git repository is
- Learn to define what a git commit it
- Identify what a git hash is
- Learn how to view the git log

## Lesson

For the uninitiated, in the story of Back To The Future, the protagonist (Marty McFly) finds himself accidentally transported from 1985 to 1955 and triggers what is known as the "Grandfather Paradox". A type of temporal complication known as an "Infinite Regression Paradox". A paradox is a contradictory statement that appears to remain true, despite its contradictions.

The grandfather paradox is best explained as: You go back in time to kill your grandfather, so you were never born, and if you were never born, you never went back and so your grandfather is alive, which means you were born, which means you go back, which means you were etc.

What happens in in the movie is, as we will see later, Marty McFly saves his father from being hit by a car in 1955, which through a sequence of events actually prevents his parents from falling in love, and he begins to fade away as his parents never married and thus Marty McFly never came to be.

Before we get to the end of Act I, however, we must fill in some details (and do things with git), so it's time to get started.

    $ mkdir bttf
    $ cd bttf
    $ git init
    
This simple command sets up the directory you are in as a git `repository`, a `repository` is a term to refer to a project managed by git. It does this by creating a directory called `.git` in the directory you are in. It's called `.git` because in Linux, Unix, MacOS, and most other computer systems, this is how a directory is hidden (Windows is different and is, to my knowledge, the only system where hiding files and folders doesn't work the same way) and since git was developed by the guy who developed Linux, to help him develop Linux, it makes sense that gits design and features work well with Linux and related systems. This directory is a database of changes to your project.

NOTE: It's important to remember that git is a change management system, it tracks changes and only changes, there's never multiple different versions of a file, but instead a number of changes to a file over time, however it's just a piece of software and doesn't have any awareness of what the nature of the changes are and can't perform miracles, it still often requires humans to make the ultimate choice when things end up in a state of conflict.

As we work through this tutorial, we will be editing a file called `HISTORY.md` to track the events of Hill Valley and our protagonist, Marty McFly. So let's create that now.

    $ touch HISTORY.md
    
Admittedly this is nothing specifically to do with git, but we needed to do some setup. Remember we have a blank git database ready to start working with. Also, something _real_ important to remember, git tracks changes to _files_, you can't add folders to git, folders are ways of storing files, and git doesn't care about folders.

I write this because it's worth _always_ remembering that git tracks changes to files and a _change_ is a bigger concept than you may immediately think. Adding a new file is a change, deleting a file is a change, editing a file is a change. Confusingly one git command handles all three: `git add`, this makes sense when you create a new file, I _guess_ makes sense that you add changes, but it's somewhat counter intuitive to add the removal of a file, but technically you're changing a project and you need to add the changes, so it logically follows, I suppose.

So to add the file to our git database we can do this:

    $ git add HISTORY.md
    
This will _stage_ the changes, a staged change is not yet committed and it represents a way to add some changes that you may not yet be ready to commit, but also don't want to loose. At this point it isn't actually committed to the git database, there's another step we need to take.

To commit our change we must use the commit instruction.

    $ git commit -m "initial commit"
    
Something to remember, a commit _must_ have a commit message and you provide it with the `-m` option, if you fail to do this, it'll enter vim and ask you to write a commit message and if you don't know vim, it'll be a little confusing. In other words, always provide the `-m` flag and provide a message.

With each subsequent change to a file we must add and commit it, using this pattern above, and you will be doing that a _lot_ during this lesson. It'll be a little bit tedious but it's important to practice.

To start we will create a table in our history file, it will be in Markdown format (which you can read aboud in the resources), this table will hold all events in the main timeline of back to the future. It's important that each event is committed individually (so that we can go back to it).

## Resources

- [Time Travel](https://plato.stanford.edu/entries/time-travel/)
- [git init reference](https://git-scm.com/docs/git-init)
- [Markdown](https://daringfireball.net/projects/markdown/)
