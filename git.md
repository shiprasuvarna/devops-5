

![image](https://github.com/shiprasuvarna/devops-5/assets/102012006/6ebd0ea4-3b51-4702-a075-816914a1ed27)
![image](https://github.com/shiprasuvarna/devops-5/assets/102012006/710e66c1-cef3-4739-8406-34a8d00bf5da)
![image](https://github.com/shiprasuvarna/devops-5/assets/102012006/f3f0995e-e170-4a53-af76-d7315e077a6a)
![image](https://github.com/shiprasuvarna/devops-5/assets/102012006/56be7c85-51c7-4ade-95b3-9bff105653cb)

1) git config
Utility : To set your user name and email in the main configuration file.
How to : To check your name and email type in git config --global user.name and git config --global user.email.    

2) git init
Utility : To initialise a git repository for a new or existing project.
How to : git init in the root of your project directory.  

3) git clone
Utility : To copy a git repository from remote source, also sets the remote to original source so
that you can pull again.
How to : git clone <:clone git url:>

4) git status
Utility : To check the status of files you’ve changed in your working directory, i.e, what all has
changed since your last commit.
How to : git status in your working directory. lists out all the files that have been changed.

5) git add
Utility : adds changes to stage/index in your working directory.
How to : git add .

6) git commit
Utility : commits your changes and sets it to new commit object for your remote.
How to : git commit -m”sweet little commit message”

7) git push/git pull
Utility : Push or Pull your changes to remote. If you have added and committed your changes
and you want to push them. Or if your remote has updated and you want those latest changes.
How to : git pull <:remote:> <:branch:> and git push <:remote:> <:branch:>

8) git branch
Utility : Lists out all the branches.
How to : git branch or git branch -a to list all the remote branches as well.

9) git checkout
Utility : Switch to different branches
How to : git checkout <:branch:> or **_git checkout -b <:branch:> if you want to create and
switch to a new branch.

10) git stash
Utility : Save changes that you don’t want to commit immediately.
How to : git stash in your working directory. git stash apply if you want to bring your saved
changes back.

12) git merge
Utility : Merge two branches you were working on.
How to : Switch to branch you want to merge everything in. git
merge <:branch_you_want_to_merge:>

14) git reset
Utility : You know when you commit changes that are not complete, this sets your index to the
latest commit that you want to work on with.
How to : git reset <:mode:> <:COMMIT:>

16) git remote
Utility : To check what remote/source you have or add a new remote.
How to : git remote to check and list. And git remote add <:remote_url:>
