---
layout: post
category: dev
---

## How to add ssh-key authentication for git repositories

As the experiment loads get heavier, I had to move into several different servers with the same experimental setups.

Because I am using private opam packages that are pinned to git repositories, everytime I try to move out, I had to set up the

SSH key authentication. 

Problem is that I keep forgetting how to do this, and google all the way again.

So, I am leaving this procedure so that I can just look this up.


### key generation
The following command will generate an SSH key to the home directory

`$ ssh-keygen -t ed25519 -C "your_email@example.com"`

passphrase could be whatever.

Then, copy the output of the command below.

`$ cat ~/.ssh/id_ed25519.pub`

### add ssh-key authentication to github

Go to Settings of your git profile and click the `SSH and GPG keys` tab on the left side.

click the green button `New SSH key` and paste the key. (key title don't matter)

This will do the trick.