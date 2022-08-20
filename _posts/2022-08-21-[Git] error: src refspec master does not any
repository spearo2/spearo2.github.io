---
layout: post
category: dev
---

## I am leaving a solution for this error which keeps happening because of my impatience.

<img src="{{site.url}}/assets/images/dev/git1.png" width="auto" height="auto" alt="git1">

The error usually occurs when I input

`$ git push origin master`

This happens when push occurs without pull. Git prevents such operations which could overwrite the history.
In my case, I will create a repo and often forget to clone or pull the branch before pushing the intialization.

So the solution is as following:

`$ git init`
`$ git add .`
`$ commit -m <whatever the message you want>`
`$ git remote add origin <URL>`
`$ git push -u origin master`

If the problem occured beacuase there was no branch (master in this case).

`$ git checkout -b 'master'`
`$ git push origin master`

However, as I explained this can occured due to various situations. So if you understand the main cause you could fix it otherwise.