<h1> Git and Github Tutorial - Part 3: Where? </h1>

We have seen how to create and use a local git repository, but now you are probably wondering where GitHub comes in. Well in this part of the workshop we will go over how to set up a remote repository to backup and protect your projects on GitHub, as well as allowing for easy collaboration between multiple people.

<h2> Spacial Layout </h2>

Now that you hopefully got some idea of how a git repository is structured in time, we can go over the relationship between local and remote repositories stored on your local machine and on github respectively.

* The <b> local </b> repository is just that, it is the repository that is stored in your working directory alongside the files that it is monitoring. Alone, it only acts to backup changes you make to your working files. Ideally, each person who is working on a given project will have their own local repository, so there can be multitudes of these in existance. If the hardware (your computer and/or its drives) are damaged, then the repository will be damaged along with them. It is also no easier for someone else to access and collaborate with than any files on your computer.
* A <b> remote </b> repoistory is a repository that is not stored on your computer, but on another server or computer somewhere. For the case of this tutorial, the remote directory is the directory that is hosted on githubs servers. There is usually only one of these in existace, which acts as the master repository which all the local repositories work off of.

Git is designed to work well in such a two repository system, however you can work with just a local repostiory and you may wish to do this for small individual projects, but remember that this is not a good backup soloution as all the data is still on your local machine.

> Activity 3.1: Create a new remote repository on GitHub. Click the new repository button in the left-hand panel of the github homepage, give your repository a name, and keep it set to public.

There are two ways to connect a local repository to a remote repository depending on which you created first.

> Activity 3.2a: *If you created the remote repository on Github first* clone the repository to your local machine with the following command:

    git clone {repository_url}
    
> Your repository url can be found on GitHub, by entering your remote repository homepage and finding the green dropdown menu called code. Copy the url under the https tab.

> Activity 3.2b: *If you created the local repository on your local machine first using git init as we did in the last tutorial* you will also need to make a remote repository seprately. Once you have create a remote repository on github you can connect your existing local repository to the remote using the following command.

    git remote add origin {repository url}

> As with 3.2b your repository url can be found on GitHub, by entering your remote repository homepage and finding the green dropdown menu called code. Copy the url under the https tab. Once you have connected your local to your remote repository, you'll want to update it with any commits you have already made to your local repository, to do this use the following command:

    git push -u origin master

Next we will want to learn how we can update the remote with changes made to the local, and vice versa. This is accomplished using two commands git push and git pull. Git status is again usefull here, as it can tell us how many commits the local is either ahead or behind the remote.

> Activity 3.3: To get any changes from the remote to your local, use the following command:

    git pull

> This is mostly usefull when working with others, or working on mutliple machines you want to keep in sync with each other. 

> Activity 3.3: To push the local repostiory changes to the remote we can use the following command.

    git push

> Not that only changes to the local repository, not the local working directory, will be pushed to the remote - so make sure you commit any changes you want to back up to your local repository first, before you push them to the remote repository. When you enter this command it will ask you for your git username and password, enter these as prompted.

<h2> Git Branching </h2>

A chain of linearly connected commits is called a <b> branch </b> typicaly the first and main branch in a repository will be known as the 'master' branch. This is often kept as a clean working copy of your code. Repositories can have multiple branches that divere from each other however. Each branch can contain a different version of the working files, and as long as these changes have been commited the user can swap between different branches.

This is most often used to create 'feature branches', where a specific feature, addition, or bug fix can be worked on without affecting the clean working copy of the master branch. When a feature is complete it can be <b> merged </b> back into the master branch (or any other branch) to update the master branch to a new working version. This can also be nested, so branches can have branches infinititum. There can also be multiple branches open for one branch at a time.

If you try to merge a branch into another but that branch has had changes since the orignal branch was split from it which contradict with the new changes you are trying to merge, this results in a <b> merge conflict </b>. In the case of a merge conflict, it requires the user to manually review the two sets of changes and selectively choose which to keep. This can result in a lot of complications, so it is still best to try and avoid working on the same bit of code twice.
