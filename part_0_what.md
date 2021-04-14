<h1> Git and Github Tutorial - Part 0: What? </h1>

This preliminary part of the Git and Github tutorial will give a brief introdution to what exactly git is. Throughout these notes there will be some amounts of information, like this, intersperced with activities which will be formatted like this:

> <b> Activity 0.0 </b> *This is an example activity. It does not require any action on your part.*

It will be best to try to complete the activities along with the workshop so that the demonstrators can help with any problems that arise. If you are are having problems, please let one of the demonstrators know. There are many free git and github tutorials avalible online, which I would encourage you to explore after completing this workshop to continue you knowledge. What this workshop hopes to achive is just an introduction to get you started.

<h2> Version Control, Git, and GitHub </h2>

The first thing to establish is the difference between Git, Github, and more broadly version control.

* <b> Version control systems </b> allow software developers to easily maintain and control different versions of their code. They allow their users to save snapshots of their code at different stages of development.
* [<b>Git</b>](https://git-scm.com) is a free open-source software control system. It is commonly found by default on many computer systems and terminals, and is used widely across both industry and academia. 
* [<b>Github</b>](https://github.com) is one of a few online services that provide hosting for github repositories (we'll go over what these are later). 

Neither git nor github are exclusively used for software development, and in fact be used to control versions of any type of file you wish. However, for the purposes of this tutorial, and because that is what Git is primarily used for, we will often talk about the more specific case of software development.

<h2> Version Control </h2>

Version control is an extremly usefull tool for those looking to develop software, as was stated, at their most basic they allow their users to save multiple versions of their code at the same time. However, it can be thought of even more simply than that - it dosn't neccisarily need to be code that you are saving. Most version control systems will allow you to keep versions of any type of file - anything in plain text of course, but binary files if the occasion arrives (although they will not neccisarily be to display the contents of those files in their interface).

These tutorials for example have been added to a git repository and uploaded to Github.

<h2> Git </h2>

[Git](https://git-scm.com) is one of many version control systems out there. It is one of the most popular, if not the most, however you may also encounter another version control system such as CVS, SVN, or another. If you know or find out your going to be using on of them don't be concerned, most verison control systems operate on similar priciples - and the intiuition on how to use them will also be transferable between systems. It is important to keep in mind that it is not the only version control system.

How exactly you use git will be dependant on your operating system:

1. If you are using <b>eOSX (Mac) or a Linux distribution </b>then you will probably already be able to access git via your terminal.

> <b> Activity 0.1a </b> *If you are using OSX (Mac) or a linux distribution then procced with this activity otherwise go to Activity 0.1b.* Open your terminal and type the following command.

    git

> If your terminal can access git this should display the git help text. If not speak to one of the demonstrators.

2. If you are using <b> Windows </b> (boo) then things are a bit more complicated.

> <b> Activity 0.1b </b> *If you are using windows*:
> 1. First head to [this link](https://git-scm.com/download/win) and download git for Windows.
> 2. Run the downloaded installer: <b> Leave all options default </b>.
> 3. Search for and open the program called: 'Git Bash'. This will open a terminal emulator which will allow you to use git from the command line.
> 4. Type the following command.

    git
    
> If your terminal can access git this should display the git help text. If not speak to one of the demonstrators.


<h2> Github </h2>

A lot of people get confused and think that Github and Git are synonymous - but they are different things. Github is a for profit company whereas git is a free open source software tool. Github allows you to store github repositories online, backing up your repositories and allowing access to them from anywhere with a free internet connection.

Github is also not the only online repository. There are other services avalible such as [GitLab](https://about.gitlab.com) and [BitBucket](https://about.gitlab.com). Each have a slightly differnt setup and set of features, but again they operate in very similar ways, and in this case they all use Git, so any commands you learn will work across all of them. Which you use is a matter of personal preference, or more often than not, a matter of which tool the organisation you work for is already using.

> <b> Activity 0.2 </b> *If you have not already* create a github account [here](https://www.github.com/join).
