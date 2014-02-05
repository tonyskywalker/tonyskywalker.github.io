git-and-github-start

I want to try git and github.

1. set up git

# Sets the default name for git to use when you commit

git config —global user.name “Your Name Here”

# Sets the default email for git to use when you commit

git config —global user.email “your_email@youremail.com”

2. password

a: Check for SSH keys

cd ~/.ssh

# Checks to see if there is a directory named “.ssh” in your user directory

b: Backup and remove existing SSH keys

ls

# Lists all the subdirectories in the current directory
# config id_rsa id_rsa.pub known_hosts

mkdir key_backup

# Makes a subdirectory called “key_backup” in the current directory

cp id_rsa* key_backup

# Copies the id_rsa keypair into key_backup

rm id_rsa*

# Deletes the id_rsa keypair

c: Generate a new SSH key

ssh-keygen -t rsa -C “your_email@youremail.com”

# Creates a new ssh key using the provided email
# Generating public/private rsa key pair.
# Enter file in which to save the key (/c/Users/you/.ssh/id_rsa): [Press enter]
Enter passphrase (empty for no passphrase): [Type a passphrase]
# Enter same passphrase again: [Type passphrase again]
Your identification has been saved in /c/Users/you/.ssh/id_rsa.
# Your public key has been saved in /c/Users/you/.ssh/id_rsa.pub.
# The key fingerprint is:
# 01:0f:f4:3b:ca:85:d6:17:a1:7d:f0:68:9d:f0:a2:db your_email@youremail.com
d: Add your SSH key to GitHub

clip < ~/.ssh/id_rsa.pub

# Copies the contents of the id_rsa.pub file to your clipboard

Go to your Account Settings

Click "SSH Keys" in the left sidebar

Click “Add SSH key”

Paste your key into the “Key” field

Click “Add key”

Confirm the action by entering your GitHub password

e: Test everything out

ssh -T git@github.com

# Attempts to ssh to github

2. create a repo

a: Create the README file

mkdir ~/Hello-World

# Creates a directory for your project called “Hello-World” in your user directory

cd ~/Hello-World

# Changes the current working directory to your newly created directory

git init

# Sets up the necessary Git files
# Initialized empty Git repository in /Users/you/Hello-World/.git/

touch README

# Creates a file called “README” in your Hello-World directory

b: Commit your README

git add README

# Stages your README file, adding it to the list of files to be committed

git commit -m ‘first commit’

# Commits your files, adding the message “first commit”

c: Push your commit

git remote add origin https://github.com/username/Hello-World.git

# Creates a remote named “origin” pointing at your GitHub repo

git push origin master

# Sends your commits in the “master” branch to GitHub

3. fork a repo

# Clones your fork of the repo into the current directory in terminal

git clone https://github.com/username/Spoon-Knife.git

