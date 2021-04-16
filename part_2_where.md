<h1> Git and Github Tutorial - Part 2: Where/When? </h1>

This section of the the tutorial will give an overview of the struture of a typical github local and remote repository setup, as well as going over how git tracks changes across time.

<h2> Basic Git Commands </h2>

A git <b> repository </b> often shortened to repo, is a database where git stores snapshots (commits) of your project. This is a place where git keeps the information about one specidic project. Usually, and optimally, each project will have its own repository (and a copy of that repository on github, but we'll get to that.).

Your <b> working tree </b> or your <b> working directory </b> contains all the files that a given git repostitory is monitoring. This is where you edit and save the files whilst you are working on them. Git monitors these files and can calculate the difference between the files and the last time you asked it to remember what the files looked like. People often get confused between git repositories and their respective working directories. The repository consists only of a folder called '.git/' within your working directory, everything else within the directory is just saved as ordinary files on your computer.

> Activity 2.1: Create a new directory using the command you learned in part 1, then navigate to it. Once you have navigated to your new directory, type the following command to intilise a git repository:

    git init

> This command creates a git repository hidden file inside your directory called .git. This repository is linked to the directory it is located, and will track changes within that file. You will not be able to see this with the ls commmand unless you add an extra tag. To see hidden files within a directory use the following command.

    ls -a
    
> If you use this command inside the directory you should see the .git repository file. If you do not see that contact a demonstrator.

Git repositories are comprised of a graph of connected snapshots or <b> commits </b>, each of these commits contains information about the changes made to your working files since the last commit. These commits are usually made manually, which we will be doing in Activity 2.2. Each commit will remember who made the commit and timestamp it. Currently your newly created git repository will have no commits.

> Activity 2.2: To get a quick summary of the current status of your repository type the following command:

    git status
    
> Currently this should show that you have 0 commits and are on the master branch. We will go over branches later. 
 
In order to make your first commit to the repository we will first need to add a new file to the directory. You may add a file to the directory however you wish too, any plaintext file will do. 

> Activity 2.2: *If you want to add a new file using the command line* you can use the following command:

    touch new_file.txt
    
> This will create a new file named 'new_file.txt'.

Once we have created a new file we can now create our first commit to the local repository. If we use the git status command you will see that the new file we have just added is now listed as untracked. This means that git has seen the new file, but we have never added it to the repository before, so any changes we make to this file will be untracked. Before we can commit to the repository we must first tell git which files we want to be included in the commit. To do this we must add the files to the <b> index </b>.

> Activity 2.3: To add an item to the index so that it is 'staged for commit' we can use the following command:

    git add new_file.txt
    
> Once we have ran that command, we can then see that git status shows us that the file is staged for commit. So we are finally ready to make our first commit.

> Activity 2.4: To commit staged changes to the repository, we can use the following command:

    git commit -m 'Commiting test file'
    
> You will notice that git forces us to use the -m tag and add a message with the commit. This is important for future reference so try to make these descriptive. If you did not use the -m tag then git will open a command line text editor (probably vim) and get to write a commmit. Do not panic - to exit vim type :q. Running the git status command should show that we now have one commit.

As well as tracking new files added to the directory git also tracks changes within files. Make an edit to the file using your prefered method. 

> Activity 2.5: *If you want to quickly change to the contents of the existing file* you can use the following command:

    echo 'This is example text.' > new_file.txt
    
> To quickly view the contents of the file use the following command:

    cat new_file.txt
    
If you run git status once you have made a change to you file you should see that it shows that the file has been modified. Add this change to the commit. Hint: you can add all tracked files to a commit at once using the -u tag:

    git add -u
    
Commit this change to the directory, remember to add a usefull message using the -m tag. 

> Activity 2.5: You can see all the past commits using the following command:

    git log
    
> Try this now, you should see the two commits you have made. The large string of numbers and letters you see after the commit are called the git hash, this is the unique identified for that commit.

Now that git is tracking changes you make to your code, if you make a mistake in your code and want to revert the changes of a particular commit, it is possible to do this. There are a few ways to go about this, but the most simple and the safest method is to use git revert. First you must commit any current file modifications to your repository. Then find the git hash you wish to revert using the git log command. Hint: This is the hash of the git you wish to revert, not the hash of a commit you wish to revert to.

>  Activity 2.6: Try reverting the last commmit you made. Find the git hash of your last commit and revert it using this command:

    git revert insert_hash_here
 
> Unfortunately this will probably open vim or whatever text editior your git is set up to use as default. Again to exit vim either hold shift and press "ZZ", or type ":q".

<h2> Git Branching </h2>

A chain of linearly connected commits is called a <b> branch </b> typicaly the first and main branch in a repository will be known as the 'master' branch. This is often kept as a clean working copy of your code. Repositories can have multiple branches that divere from each other however. Each branch can contain a different version of the working files, and as long as these changes have been commited the user can swap between different branches.

This is most often used to create 'feature branches', where a specific feature, addition, or bug fix can be worked on without affecting the clean working copy of the master branch. When a feature is complete it can be <b> merged </b> back into the master branch (or any other branch) to update the master branch to a new working version. This can also be nested, so branches can have branches infinititum. There can also be multiple branches open for one branch at a time.

If you try to merge a branch into another but that branch has had changes since the orignal branch was split from it which contradict with the new changes you are trying to merge, this results in a <b> merge conflict </b>. In the case of a merge conflict, it requires the user to manually review the two sets of changes and selectively choose which to keep. This can result in a lot of complications, so it is still best to try and avoid working on the same bit of code twice.

<h2> Spacial Layout </h2>

Now that you hopefully got some idea of how a git repository is structured in time, we can go over the relationship between local and remote repositories stored on your local machine and on github respectively.

* The <b> local </b> repository is just that, it is the repository that is stored in your working directory alongside the files that it is monitoring. Alone, it only acts to backup changes you make to your working files. Ideally, each person who is working on a given project will have their own local repository, so there can be multitudes of these in existance. If the hardware (your computer and/or its drives) are damaged, then the repository will be damaged along with them. It is also no easier for someone else to access and collaborate with than any files on your computer.
* A <b> remote </b> repoistory is a repository that is not stored on your computer, but on another server or computer somewhere. For the case of this tutorial, the remote directory is the directory that is hosted on githubs servers. There is usually only one of these in existace, which acts as the master repository which all the local repositories work off of.

Git is designed to work well in such a two repository system, however you can work with just a local repostiory and you may wish to do this for small individual projects, but remember that this is not a good backup soloution as all the data is still on your local machine. There are a few commands to remember about

