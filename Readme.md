# HWGitHub
This is a POC of how to use two separate workspaces to synchronized
with a remote repository

Assume you have two developers, Alice and Bob, each with their own workspace and a remote GIT repo.

Alice and bob both run git log and both see the same changes. Both users have exactly the same files in their 
local repos.

$ git log --oneline
ef33e66 added Readme.md at top of project
f833327 added world
0b08c00 add eclipse project settings
5bf1481 initial commit

## Change 1. 
Alice edits Readme.md, adds it to the change list and commits it. Alice then runs git push to push the change to the repo.

Question: What happends when Alice and Bob run git status?
Answer: Both see the exact same thing 

	On branch master
	Your branch is up-to-date with 'origin/master'.

 	In the case of Bob, this is NOT accurate.

How to fix:
	If bob rus "git fetch" this pulls down changes from the remote repo, but does not merge them
	Next, bob runs git status to check the status, or bob views the history
	He will see a new change

There is a difference between remotes/origin/master and local

$ git log --oneline -n 3
ef33e66 added Readme.md at top of project
f833327 added world
0b08c00 add eclipse project settings

git log --oneline -n 3 remotes/origin/master
e565054 add scenario 1
ef33e66 added Readme.md at top of project
f833327 added world


Let me see what happens now...




