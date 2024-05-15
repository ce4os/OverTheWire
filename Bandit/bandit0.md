Bandit Level 0 - Welcome to ssh!
================================

[Level 0](https://overthewire.org/wargames/bandit/bandit0.html)

Goal
----

Log into the game (a remote machine) on

Host: bandit.labs.overthewire.org 
Port: 2220
Username: bandit0
Password: bandit0

Solution
--------

Requirements: 

- Linux Terminal 
- SSH Client 

```sh
# Syntax
# ssh username@servername_or_ip -p portnumber
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

You will be prompted for a password (which is not displayed -
this is a security feature and known as password hiding/masking.
Essentially it prevents someone peeking over your shoulder reading 
your password). Type in bandit0. You will be logged in to the remote
machine and greeted. 

Congrats! You used ssh for the first time. 

To logout simply type in 
```sh
bandit0@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
```

