![Back to the feature branch logo](bttfb.png)

# Part 2: Time travel with style

Great Scott! Marty McFly must be very confused, one moment he's fleeing for his life in 1985, the next he's thrust back to 1955! Whatever will he do? More to the point, how do we join him in 1955?

Well, git is our DeLorean here, and we can use it follow him to 1955, that's real heavy!

So this is where it's important that you have followed [part1](part1.md) and have committed each event as you go, because we need to use these commits to jump back to 1955, if you haven't done this, you'll have to restart and try again, heavy!

Tip: Each git commit has a `commit hash` which uniquely identifies each commit, we can use these to move back to a specific point in the history of the project.

The act of Marty McFly arriving in 1955 in the Back To The Future universe results in a divergent timeline (or a branch) where a number of events either didn't happen, or happened differently, and some events may happen in this timeline/branch that didn't originally happen.

He arrives at precisely 0615 on Saturday November 5th 1955, so you will need to find the `git hash` of a commit just before that, to have a look at the history of the git project you can check out its log.

    $ git log
    
The format of the log is as follows, I have only included the 3 most recent commits but we need to understand what we are looking at:

    commit 28f96291212db91b342854ffa8ff6bae43994231 (HEAD -> main)
    Author: NMunro <neilmunro@gmail.com>
    Date:   Thu Mar 28 00:16:12 2024 +0000

        Marty accidentally uses time machine to go back to 1955

    commit 949771034a7fe77ba834422ec738fca371db94f4
    Author: NMunro <neilmunro@gmail.com>
    Date:   Thu Mar 28 00:14:58 2024 +0000

        Doc Brown shot dead by Libyan terrorists

    commit a2f21a8c6664ae6d932d6e9ab406bef923ef9900
    Author: NMunro <neilmunro@gmail.com>
    Date:   Thu Mar 28 00:14:06 2024 +0000

        Einstein arrives one minute into the future

# Resources
