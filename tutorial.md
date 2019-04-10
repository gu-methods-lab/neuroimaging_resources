# Learning git
# Git is all about VERSION CONTROL!

cd "/some/directory"
git init #creates a new subdirectory named .git that contains all of your necessary repository files

######
# if you want to start version-controlling existing files (as opposed to an empty directory), you should probably begin tracking those files and do an initial commit.
git add file.sh
git add README.md
git commit -m 'initial project version'
######

# instead, will clone and existing GitHub repository
git clone https://github.com/gu-methods-lab/neuroimaging_resources neuroimaging_resources

# Let's check the status of our repository
git status

# let's change the file README.md
# add your name to the contributors list
# Now, let's check the status of our repository
git status

# You should see "modified:		README.md"
# We can also quickly see our changes from the command line
git diff

# Let's create a new file called list_of_resources.md
echo Here is a list of neuroimaging resources > list_of_resources.md

# Let's check the status of our repository, after we added this file
git status

# Notice that "list_of_resources.md" is listed as an untracked file
# Let's begin tracking it so it will be staged to be committed later
git add list_of_resources.md

# Let's check the status of our repository again
git status

# Notice that list_of_resources.md is now listed as a new file
# Remember that you can move or remove files all the same!

# Let's commit our changes
git commit -m "added name to contributors; created list of resources"

# We can look at our commit history now
git log

# Or more elegantly:
git log --pretty=oneline

# Or even more elegantly:
git log --pretty=format:"%h - %an, %ar : %s"

# Now let's git push
# Change your user email first for privacy
git config --global user.email "username@users.noreply.github.com"

# Now let's push (might ask for username and password)
git push

# Remember:
git add file.md
git commit -m "added file"
git push

# Now, I will push something new. 
# Now, you pull!
git pull

# It's usually better to work in a branch (not the master branch)
git checkout -b branch1