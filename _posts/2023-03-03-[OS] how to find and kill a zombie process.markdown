---
layout: post
category: dev
---

# [OS] how to find and kill a zombie process

## Zombie process

A zombie process is a process that has completed execution but still has an entry in the process table.</br> This happens when a parent process does not wait for its child process to complete execution and the child process becomes a zombie process.

## How to find a zombie process

If it is a ubuntu system, you will see this kind of message when you log in.

<img src="{{site.url}}/assets/images/dev/zombie1.png" width="auto" height="auto" alt="zombie1">

You can also use `ps` command to find zombie processes.

`$ ps aux | grep 'Z'`

Following command will give a table of pids with stat 'Z'</br>
The 7th column is the STAT column.

USER       PID     %CPU %MEM  VSZ    RSS TTY      STAT START   TIME COMMAND</br>
root       1       0.0   0.0  1836   648 ?        Z   00:00   0:00 /sbin/init</br>
root       2       0.0   0.0     0     0 ?        Z    00:00   0:00 [kthreadd]</br>

The table looks something like this.</br>
We see that we have 2 processes with stat 'Z', meaning that they are zombie processes.</br>

Now, killing a zombie process won't solve the problem. You need to find the parent process and kill it.

`$ pstree -p -s 1`

This will show 
something like this.

`init(1)---cnid_metad(3)---cnid_dbd(4)`

Then, kill the parent process.

`$ kill -9 4`




