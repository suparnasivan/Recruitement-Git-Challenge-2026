# Commands I used for this task

git clone <url>
- copies the repo from github onto my laptop, i used this to get the forked repo locally

git status
- just shows me what changed/what's tracked or not, i used this a bunch of times to check before committing

git add <file>
- stages the file so git knows to include it in the next commit. before this the file is just sitting there untracked

git commit -m "msg"
- actually saves the staged changes as a commit in the history, moves main/whatever branch forward by one commit

git config --global user.email "..."
git config --global user.name "..."
- had to run this first because git didnt know who i was, wouldnt let me commit without it

git branch Suparna
- made a new branch called Suparna, this doesnt move me onto it, just creates the pointer

git checkout Suparna
- switches me onto that branch so now whatever i commit goes there instead of main

git merge Suparna
- brought the Suparna branch changes back into main, since i hadnt made new commits on main in between it just fast forwarded (no merge commit needed)

git reset --soft HEAD~1
- used this to undo the favourite dish commit. soft reset means it removes the commit from history but keeps the file and the changes staged, nothing actually got deleted

git rm favourite_dish.txt
- the reset left the file just sitting there staged, it didnt delete it. so i had to remove it myself with this command

git commit -m "Remove favourite dish file"
- committed that removal so the file would actually be gone, since reset --soft alone doesnt delete anything from my machine

git log --oneline
- checked this after the reset to confirm the commit was actually gone from history

git push origin main
- pushes all my local commits up to my fork on github so they show up online
