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

There will be many more advantages that I've forgotten to list here but the point is that the benifits are innumerable, and they become even greater the larger and more complex a project you are working on. Any serious software development done by anyone in academia or industry will use some kind of version control system.

<h2> Backup </h2>

More simple to see than the benifits of version control are the benifits of having a version of your code backed up on a remote server, Things can, and often do, happen to make you lose or damage your code stored on a local machine. Using remote repository services like Github that you always have a copy of your code avalible even if your local copy is corrupted. (Although it would also be prudent to keep your own backups as well as no backup option is 100% and the more backups the better).

<h2> Collaboration </h2>

Another large reason to use version control is to allow for easy collaboration between multiple developers. When you are the only person working on a codebase this is not such a problem - however as soon as you start working on a project with at least one other person you will start to see issues arise.

* If you are both working on the same code at the same time than whoes is the main version of the code?
* How will you resolve conflicts if both of you try to change the same code at once?
* How will you make sure you your version of the code won't diverge massivelty over time.

This tutorial will not be talking about how to collaberate with Git in great detail, rather first focusing on how to use it for indvidual use. However, once you've got the basics paracticed it will be much easier to move into a colabarative working environment.

<h2> Terminal Commands </h2>

This workshop will focus on using Git from the command line as this is the most widely avalible and uniform method to use git. There are GUI alternatives such as [GitHub Desktop](https://desktop.github.com) if you wish to investigate them feel free, they have most of the same functionality and still use Git at their core. However I would reccomend learning to use the terminal if you want to persue a career in coding, and for the purposes of this workshop that is what we will be using.

For those of you who are unfamiliar with using the command line this section will breifly go over some very basic commands just to get you started. These commands are not exclusive or related to Git, but they will help you navigate the interface.

The command line is a method to send commands to a computer via text entry rather than by navigating via a gui. In the end both methods can send commands for the computer to execute, however it is often quicker to execute complex commands via the command line.

> Activity 1.1 Find your current working directory by typing the following command:

		pwd

> All commands you run will execute as if they are being run in your current working directory:
    
> Activity 1.2 List the contents of your current working directory by entering:

		ls
 
> This shows the contents of your current working directory.

> Activity 1.3 Make a new folder within your current directory by typing the following command:

		mkdir test_directory
		
> this will make a directory called test_directory. If you type ls again you should be able to see this new directory. You can name a new directory whatever you like by changing test_directory to another name. Hint: refrain from using spaces in file and folder names, it gets annoying.

> Activity 1.4 Change your current working directory to the new directory by typing:

		cd test_directory
		
> Once you have changed your working directory you should be able to see that it is empty by typing ls. You can see you have moved to the correct directory by typing pwd. To exit the directory again type:

		cd ..
		
> This will move you up one level of the directory tree back to your original working directory.

> Activity 1.5 To delete a directory use the following command:

	rm -r test_directory
	
> The -r tag ensures that the folder is deleted recursively. Warning this will also delete all the directory contents so be carefull.

Congratulations you can now navigate your computer using the command line. We will use these commands in the next tutorial, so be sure to keep this page open unless you have a good memory.
