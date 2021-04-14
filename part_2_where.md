<h1> Git and Github Tutorial - Part 2: Where/When? </h1>

This section of the the tutorial will give an overview of the struture of a typical github local and remote repository setup, as well as going over how git tracks changes across time.

<h2> Temporal Layout </h2>

A git <b> repository </b> often shortened to repo, is a database where git stores snapshots (commits) of your project. This is a place where git keeps the information about one specidic project. Usually, and optimally, each project will have its own repository (and copies of that repository on github, but we'll get to that.).

Your <b> working tree </b> or your <b> working directory </b> contains all the files that a given git repostitory is monitoring. This is where you edit and save the files whilst you are working on them. Git monitors these files and can calculate the difference between the files and the last time you asked it to remember what the files looked like. People often get confused between git repositories and their respective working directories. The repository consists only of a folder called '.git/' within your working directory, everything else within the directory is just saved as ordinary files on your computer.

Git repositories are comprised of a graph of connected snapshots or <b> commits </b>, each of these commits contains information about the changes made to your working files since the last commit. These commits are usually made manually, and we will be going over how to do that in part 3. Each commit will remember who made the commit and timestamp it.

A chain of linearly connected commits is called a <b> branch </b> typicaly the first and main branch in a repository will be known as the 'master' branch. This is often kept as a clean working copy of your code. Repositories can have multiple branches that divere from each other however. Each branch can contain a different version of the working files, and as long as these changes have been commited the user can swap between different branches.

This is most often used to create 'feature branches', where a specific feature, addition, or bug fix can be worked on without affecting the clean working copy of the master branch. When a feature is complete it can be <b> merged </b> back into the master branch (or any other branch) to update the master branch to a new working version. This can also be nested, so branches can have branches infinititum. There can also be multiple branches open for one branch at a time.

If you try to merge a branch into another but that branch has had changes since the orignal branch was split from it which contradict with the new changes you are trying to merge, this results in a <b> merge conflict </b>. In the case of a merge conflict, it requires the user to manually review the two sets of changes and selectively choose which to keep. This can result in a lot of complications, so it is still best to try and avoid working on the same bit of code twice.

<h2> Spacial Layout </h2>

Now that you hopefully got some idea of how a git repository is structured in time, we can go over the relationship between local and remote repositories stored on your local machine and on github respectively.

* The <b> local </b> repository is just that, it is the repository that is stored in your working directory alongside the files that it is monitoring. Alone, it only acts to backup changes you make to your working files. Ideally, each person who is working on a given project will have their own local repository, so there can be multitudes of these in existance. If the hardware (your computer and/or its drives) are damaged, then the repository will be damaged along with them. It is also no easier for someone else to access and collaborate with than any files on your computer.
* A <b> remote </b> repoistory is a repository that is not stored on your computer, but on another server or computer somewhere. For the case of this tutorial, the remote directory is the directory that is hosted on githubs servers. There is usually only one of these in existace, which acts as the master repository which all the local repositories work off of.

Git is designed to work well in such a two repository system, however you can work with just a local repostiory and you may wish to do this for small individual projects, but remember that this is not a good backup soloution as all the data is still on your local machine. There are a few commands to remember about

