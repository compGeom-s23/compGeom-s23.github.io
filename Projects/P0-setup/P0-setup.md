
# Setup 


**Slack**

We'll be using Slack for communication. The advantage of using Slack over email is that it keeps all messages in one place,  it's easy to keep conversations organized, and has a lot more cool options .  If you want to send me a private message, Slack has the option of a "direct message (DM)". You can DM me, or anyone else in the class. And you can create your own channels, which can be private, to which you can invite your team mates (for e.g. when team-working on a project! really cool feature!). 

I created three channels: #projects (for all project-related communication), #general (for class materials and general announcements), and #random (for everything else).

***

**Unix crash course**

Go through the Unix [crash course](https://tildesites.bowdoin.edu/~sbarker/unix/)  maintained by Sean Barker. You don't need to know everything upfront, but starting week 2 being familiar will greatly help.

Nothing to submit. As always, if you run into problems, post on Slack!

***

**Compiling and running a C/C++ program from the terminal**

Create a program that writes `Hello World'  and compile it and run it from the terminal, first by hand and then with a Makefile (which you create). To see how, follow the steps in the Unix crash course, above.  

Nothing to submit, just warmup. 

***


**Version Control with Git**

Some of you may be familiar with Git and Github from Systems. If so, go quickly over this section to refresh your memory and make sure you don't miss anything. If this is the first time you see Git, you may want to check out the detailed [Git tutorial](https://tildesites.bowdoin.edu/~sbarker/unix/git.html) maintained by Sean Barker.

[Git](https://git-scm.com/) is an open-source, distributed version control software, initially developed by Linus Torvalds for Linux. [GitHub](https://github.com/)  implements a web-based version of git where users, in addition to using git commands, can store their repositories "into the cloud". GitHub offers all the functionality of git plus extra features (like wiki pages for each project; networking features like feeds and followers). GitHub has 20+ million users, and it's become a virtual meeting place for software developpers, for sharing information and showcasing projects.

How it works, in a nutshell: With Github you and your peers can work together on projects from anywhere in the world. Initially you (or someone else) will create a remote master repository for your project. This master repository is hosted remotely, on github. You (and your partners, if any) will then clone (checkout) a private copy of the remote master repository on your local machine. You can clone several copies of the master repo in several locations, if you want. You can make changes to your local copy. When you are done, you stage these changes for commit, and then you push them to the master repository. Once your changes are pushed to the master repo, your partners can get them by "pulling" the changes from the master repo into their local repo. Git automatically merges the changes pulled form the master with the local changes in the local repo. Git keeps a record of all changes, and any change can be reverted.

To start, create a Github account, if you don't have one already. Before you starting using the Git command on the command line, you need to give it a basic configuration. This will tell Git who you are, making it easy for you and your partners to identify who committed code to your shared repository. Replace the email and name strings with your email address and name. If you have not run these commands, then the very first Git commit will fail and tell you to run them.

```
git config --global user.email "username@bowdoin.edu"
git config --global user.name "Your Name"
git config --global push.default simple
```

**Set up authentication with SSH-key**

With Github you can authenticate with a password, or with an SSH-key; the latter is more secure and might become required, so it's worth taking the time to set it up.
To authenticate using an SSH-key, a user must have an SSH-key pair on their local computer. An SSH-key consists of a private key and a public key. The public key can be shared with anyone, and the private key needs to be kept confidential (just like a password).

How it works:

When the user (the client) wants to connect to the server (the host) vis SSH-key authentication, it will send her public key to the host.
The host will will generate a random string and it will encrypt it with using the public key. This encrypted message can only be decrypted with the associated private key.
The host will send this encrypted message to the user's client to test whether they actually have the associated private key.
The client will decrypt the message using the private key and obtain the random string, and send it back to the host.
The server compares the string received from the client with the original string, and determines whether the client has the private key.


Setting up SSH-key authentication in Github:

- __Check to see if you have an SSH-key and if not, generate one:__

If you have one, it must be in `~/.ssh/;` If you see an `id_rsa.pub` file, or something like this, it means you already have a public key. If you don't see one, then generate one. 

To generate an SSH-key: In the terminal, use the `ssh-keygen` command. SSH keys are 2048 bits by default; To specify a larger number of bits, include the -b argument followed by the number of bits you would like. We'll use 4096 as per Githib's recommendation.

```
ssh-keygen -t rsa -b 4096 -C "youremail@bowdoin.edu" 
```
This uses the RSA algorithm and creates a new public/private SSH key pair on your computer, using the provided email as a label. When it prompts you to enter a file to save the key, press Enter to accept the default. At the next prompt, type a secure passphrase. A passphrase should be hard to guess, have at least 15 characters, contain a combination if letters and diGits and punctuation characters.
This has generated an RSA SSH key pair, located in the `.ss`h hidden directory in your home directory. These files are:

```
~/.ssh/id_rsa    <------------ the private key. DO NOT SHARE!!!
~/.ssh/id_rsa.pub   <--------- the associate public key. This can be shared freely 
```

- __Configure your SSH-client on the machine from where you connect to Github, to use your SSH-key for authentication:__

To do that, modify your `~/.ssh/config` file to automatically load keys into the SSH-agent and store passphrases in your keychain. You can do this with your favorite editor (for e.g. nano, atom, emacs, vim ). If this file does not exist, you need to create it.

```
Host github.com
      AddKeysToAgent yes
      UseKeychain yes
      IdentityFile ~/.ssh/id_rsa
```      
If you had to create your SSH config file, you'll also need to set the file permissions appropriately:

```
chmod 600 ~/.ssh/config
```

- __Configure Github to use your SSH-key for authentication:__

To do that go to you GitHub account page. In the upper-right corner, click your profile photo and click Settings. Click SSH and GPG keys. Click "New SSH key". In the In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key "Personal MacBook Air". Paste in the contents of your public key file (not your private key file!). You can display the contents of your public key file, assuming that your public key is named ~/.ssh/id_rsa.pub:

```
cat ~/.ssh/id_rsa.pub
```

Paste the output of that command (using your actual filename) into the Key field of the GitHub settings page, then click Add SSH key.

You are now all set to use SSH-key authentication with GitHub. When you clone a project, you'll need to go to the GitHub repository code page and copy the SSH URL rather than HTTPS (it will look something like `git@github.com/some-organization/some-repo-name` - don't change any part of this). Use this URL in your initial clone command, and you should never need to enter a username or password for GitHub. Note that you may need to enter "yes" to accept the key the first time you run a `git` command that uses the key (most likely the initial `git clone`).



**Working with Git/Github**

If you work on an existing repository (this will be the case for the assignments in this class), you'll start by cloning the master repository. You'll receive a link for a GitHub repository that contains starter code. For example, here is a repository which holds a Helloworld program:

```
git@github.com:lauratoma/helloworld.git
```

First you will go to the path where you want to place your local directory. For example, I have a directory called `CompGeom` on my Desktop:

```
cd ~/Desktop/CompGeom
```

Now clone it:

```
git clone git@github.com:lauratoma/helloworld.git
```

This will create a folder called `helloworld`, with a file `hello.c` inside it.

```
cd helloworld
ls
hello.c
README.md
```

Once cloned, the usual work cycle in Git is __pull-add-commit-push__:

- Always start by pulling the most recent version from the master (if you don't have a partner, this is not necessary unless you pushed changes from a different repo; but it's always safe to do it and it is good practice).

```
cd ~/Desktop/helloworld
git pull
```
Now your local repo is sync-ed with the master repo.

- Now you can start working on the project: edit existing files and create new files. When you are done do a git status to find out the status of your repo:
```
 git status 
 ```
this will show you what files are modified. Now stage the files that you want to commit. For example let's say you modified hello.c. You'll want to stage it:
```
git add hello.c
```
Note: You should never add object files (.o files) and executables to the repo.

- Commit to your local repo:
```
git commit -m "describe what the changes represent"
```

Note that commit does not take file names as arguments, and will update the local repo with the files that have been staged. Files that have not been specifically staged for commit, will not be commited.

- Push the changes to the master repo:
```
git push 
```
Again, git push does not take file names as arguments; it will sync the master repo with the commited files in the local repo.
There are more advanced featured of git which you may or may not need later, like branching, resolving merge conflicts, reversing changes, deleting files, and more ---- we'll figure those out later when the need arises. For now these basics commands will suffice.

*** 
That's it for now!
