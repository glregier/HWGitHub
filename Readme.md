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
Answer:

