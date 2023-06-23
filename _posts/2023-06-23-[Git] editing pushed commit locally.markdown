---
layout: post
category: dev
---

# How to rollback push that is changed on a branch

<br>
The following command will show the most recent to second last commit pushed to the branch you are working on.
<br>
```
$ git rebase -i HEAD~2
```
if 2 is changed to different number it will show the <num>th most recent commit in an editor like the following.

<img src="{{site.url}}/assets/images/dev/git2.png" style="border:white;" width="300" height="300" alt="git2">

change "pick" of the commit that you wanna delete to "drop" according to the instruction in the editor, and save the file.

check the log with
```
$ git log
```

if you checked the corresponding commit is deleted, 

```
$ git push -f <remote> <branch>
```

Then, force push to the branch you are working on


voila