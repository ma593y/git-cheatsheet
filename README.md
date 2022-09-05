# Git-Cheatsheet-And-Practice-Repo
Git is a free and open source version control system for codebases. It's a tool that helps you manage your codebases and lets you collaborate in a very simple and easy way. It is being used by almost everyone in the software industry and it's one of the essential skill that is required for the relevant roles. I'm sharing a cheatsheet for the most important and commomly used Git commands for you to learn and practice it.

#### Commands for Git Configuration:
	
	# Configure name of the user globally
	git config --global user.name "[name]"
	
	# Configure email of the user globally
	git config --global user.email "[email address]"

#### Commands to Create Repository:

	Way 1:
		# Initialize a local repo
		git init <directory>
		
		# AND
		
		# Add the remote repo to the local repo
		git remote add origin [url]
	
	Way 2:
		# Clone the remote repo locally
		git clone [url] <directory>

#### Commands to Manage Branches:

	# List all local branches and current one with * sign
	git branch

	# List all remote or local branches and current one with * sign
	git branch -a

	# Create a new branch
	git branch [branch-name]
	
	# Delete a branch
	git branch -d [branch-name]
	
	# Checkout to the specified branch
	git checkout [branch-name]
	
	# Create & Checkout to the new branch
	git checkout -b [branch-name]
	
	# Merge the specified branch to the current one
	git merge [branch-name]

#### Commands to Make Changes:
	
	# Show modified files in working directory and staged files
	git status
	
	# Diff of what is changed but not staged
	git diff
	
	# Diff of what is staged but not yet commited
	git diff --staged
	
	# Add files to the staged area
	git add [file/files/directory]
	
	# Unstage a file while retaining the changes in working directory
	git reset [file]
	
	# Commit your staged content as a new commit snapshot
	git commit -m "[descriptive message]"

#### Commands to Inspect & Compare:
	
	# Show all commits for the current branch
	git log
	
	# Show each commit as a single line
	git log --oneline
	
	# Show the commits on branchA that are not on branchB
	git log branchB..branchA

	# Show the commits that changed file, even across renames
	git log --follow [file]

	# Show the diff of what is in branchA that is not in branchB
	git diff branchB...branchA

	# Show any object in Git in human-readable format
	git show [SHA]

#### Commands to Synchronize Changes:

	# Add a git URL as an alias
	git remote add [alias] [url]
	
	# List named remote repositories
	git remote -v

	# Fetch down all the branches from that Git remote
	git fetch [alias]

	# Merge a remote branch into your current branch to bring it up to date
	git merge [alias]/[branch]

	# Transmit local branch commits to the remote repository branch
	git push [alias] [branch]
	
	# Pusl commits on all local branches to remote repository
	git push --all

	# Fetch and merge any commits from the tracking remote branch
	git pull
	
	# 
	git pull [branch_name] [remote_URL/remote_name]

#### Commands to Rewrite History:

	# Apply any commits of current branch ahead of specified one
	git rebase [branch]

	# Clear staging area, rewrite working tree from specified commit
	git reset --hard [commit]

#### Commands for Temporary Commits:

	# Save changes of tracked files
	git stash

	# Save changes of tracked and untracked files
	git stash -u

	# Save changes of tracked, untracked and ignored files
	git stash -a
	
	# List stack-order of stashed file changes
	git stash list
	
	# Pop & apply changes from top of stash stack
	git stash pop
	
	# Pop & apply changes from the specified index of stash stack
	git stash pop <stash@{index}>
	
	# Discard the changes from top of stash stack
	git stash drop
	
	# Discard changes from the specified index of stash stack
	git stash drop <stash@{index}>
	
	# Delete all of the stashes
	git stash clear
