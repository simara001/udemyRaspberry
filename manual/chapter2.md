### GIT

#### Why is it important?

First, `Git` empowers you to make commits any time you feel like it, even when you're not connected to the network. That's pretty great. Say, you're on an airplane, or doing a some extra work on the train ride home from work, and you're at a perfect point to do a commit before moving on to the next batch of work. If you're using a centralized VCS, like Subversion, you're stuck if you can't connect to the server. You simply can't commit until you get somewhere where you have connectivity. With `Git`, you can commit immediately, network or no network. (Not to mention other tasks such as *branching*, *merging*, etcetera.)

Second, `Git` has cheap *branching* and *merging*. Though other VCSes have branching and merging, Git's branching is so good and so well implemented, you'll actually use branches frequently, and it'll make your life better. I think you'll be surprised how great it is, and how "cheap" it is (in terms of effort and complexity). We'll get into the details of how branching in Git works further along.

Third, `Git` enables you to use more flexible workflows that help you work better, smarter, and with less overall stress. That too we'll delve into in detail further along. And of course, if you're not using any version control system (and, no, manually making copies of your files doesn't count), then Git will help you manage your code and improve your workflow in ways that will blow your mind. Trust me. You're really missing out.

Aside from making your life easier, Git has a number of other benefits, including:

+ Data redundancy and replication -- Since there are multiple full repositories on multiple machines (instead of one central repository), the risk of project loss due to server failure or some other catastrophe is much lower.
+ High availability -- Server down? Network down? No problem. Work in your repo (commit, view history, branch, etc) to your heart's content. Try that with Subversion!
+ Only one .git directory per repository -- Versus a .svn in every subfolder, which, as you may know from painful personal experience, can lead to problems.
+ Superior disk utilization and network performance
+ Properties such as ignores are much easier to manage than in Subversion
+ Collaboration Friendly -- Git makes it easy to collaborate on projects with groups of
contributors. And with great services like Github, Git's collaboration friendliness is even
further magnified.
+ Not just for code! -- Git is great for all sorts of projects, not just hacking code. For
example, all of Gitology's written content is managed with Git, not just it's code.
￼

#### GIT Main Commands

`$ git init`: Initializes a new Git repository. Until you run this command inside a repository or directory, it’s just a regular folder. Only after you input this does it accept further Git commands.

`$ git config`: Short for “configure,” this is most useful when you’re setting up Git for the first time.

`$ git help`: Forgot a command? Type this into the command line to bring up the 21 most common git commands. You can also be more specific and type “git help init” or another term to figure out how to use and configure a specific git command.

`$ git status`: Check the status of your repository. See which files are inside it, which changes still need to be committed, and which branch of the repository you’re currently working on.
git add: This does not add new files to your repository. Instead, it brings new files to Git’s attention. After you add files, they’re included in Git’s “snapshots” of the repository.

`$ git commit`: Git’s most important command. After you make any sort of change, you input this in order to take a “snapshot” of the repository. Usually it goes git commit - m “Message here.” The -m indicates that the following section of the command should be read as a message.

`$ git branch`: Working with multiple collaborators and want to make changes on your own? This command will let you build a new branch, or timeline of commits, of changes and file additions that are completely your own. Your title goes after the command. If you wanted a new branch called “cats,” you’d type git branch cats.

`$ git checkout`: Literally allows you to “check out” a repository that you are not currently inside. This is a navigational command that lets you move to the repository you want to check. You can use this command as git checkout master to look at the master branch, or git checkout cats to look at another branch.

`$ git merge`: When you’re done working on a branch, you can merge your changes back to the master branch, which is visible to all collaborators. git merge cats would take all the changes you made to the “cats” branch and add them to the master.

`$ git push`: If you’re working on your local computer, and want your commits to be visible online on GitHub as well, you “push” the changes up to GitHub with this command.
`$ git pull`: If you’re working on your local computer and want the most up-to-date version of your repository to work with, you “pull” the changes down from GitHub with this command.

#### Free options in the market
Basically you have 2 free options available on the market:
**Bitbucket**: free for 5 developers unlimited number of private projects. If you need more developers involved on the projects you have, you need to pay for it.
**Github**: unlimited number of developers, unlimited number of public projects. If you need private projects, you need to pay for it.

#### Make it work

##### Installing GIT on your raspberry

The first step is to check if it is already installed.
```bash
$ which git
```

If you see a path similar to the next *snippet* you are good to go:

```bash
$ which git
> /usr/bin/git
```

If you don't, install it:

```bash
$ sudo apt-get install -y git-core 
$ which git
```

#### Add files to the project on your raspberry

The first step would be to go to *Bitbucket* or *Github* and create a repo. After you create the repo, please copy and paste the url of your repo and follow the next steps:

```bash
$ mkdir testDir && cd testDir
$ touch readme.txt
$ git init
# you only need to configure this couple of things once
$ git config –global user.email “simaratesting@gmail.com” 
$ git config –global user.name “simara testing”
$ git add .
$ git commit –m “initial commit”
# you will need to paste the line you copied from bitbucket
$ git remote add origin https://simaratesting@bitbucket.org/simaratesting/testingraspberry.git $ git push –u origin master
# enter the password you put when your bitbucket account was created
```

#### Add SSH Key into your account

Get sure you have SSH

```bash
$ ssh –v
```

Set up your default identity

```bash
$ ssh-keygen # enter
# enter
# enter
```

Copy the keys from your Raspberry:

```bash
$ cat ~/.ssh/id_rsa.pub
```

Go to *Bitbucket* or *Github* and paste your `ssh-key`.









