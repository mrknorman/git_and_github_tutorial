<h1> Git and Github Tutorial - Part 1: Why? </h1>

This first part of the tutorial attempts to justify the reasons why git, and version control in general, is such a benificial concept if your coding anything more complex than the most very basic code.

There are three main justifications for using a version control system like git:
* Version Control (quite obviously)
* Backup 
* Collaberation

<h2> Version Control </h2>

As was mentioned in part 0, git is a version control system. Version control systems allow their users to take and save snapshots of a given file structure at differing points in time. Most often this is used to track the changes to a working project either as it is first generated, or as it is maintained an evolved over time beyond the point of inital coding - (often of course the former followed by the latter).

There are several advanatages to such a snapshoting system:
* Whilst you are editing software to add new features or fix existing (or new) bugs, you can ensure that there is always a working stable code avalible for thoes who need it.
* If in the process of making additions to your software, you irrepariably break something, you can revert back to a previous versions of the code that you know is working.
* It provides a method for saving and labeling different versions of code so you know exactly what code was used to run a certain analysis.
* You can maintain several versions of the code at once, each which you know can do specific things correctly <-- This is probably not the best practice.
* You can cycle back through past changes to find out when and where a bug was introduced to the code (and who to blame).

There will be many more advantages that I've forgotten to list here but the point is that the benifits are innumerable, and they become even greater the larger and more complex a project you are working on. Any serious software development done by anyone in academia or industry will use some kind of version control system. ß

<h2> Backup </h2>

More simple to see than the benifits of version control are the benifits of having a version of your code backed up on a remote server, Things can, and often do, happen to make you lose or damage your code stored on a local machine. Using remote repository services like Github that you always have a copy of your code avalible even if your local copy is corrupted. (Although it would also be prudent to keep your own backups as well as no backup option is 100% and the more backups the better).

<h2> Collaberation </h2>

Another large reason to use version control is to allow for easy collaboration between multiple developers. When you are the only person working on a codebase this is not such a problem - however as soon as you start working on a project with at least one other person you will start to see issues arise.

* If you are both working on the same code at the same time than whoes is the main version of the code?
* How will you resolve conflicts if both of you try to change the same code at once?
* How will you make sure you your version of the code won't diverge massivelty over time.

This tutorial will not be talking about how to collaberate with Git in great detail, rather first focusing on how to use it for indvidual use. However, once you've got the basics paracticed it will be much easier to move into a colabarative working environment.
