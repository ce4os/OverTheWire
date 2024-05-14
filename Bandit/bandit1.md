Bandit Level 1 - Reading a file
===============================

[Level 1](https://overthewire.org/wargames/bandit/bandit1.html)

Goal
----

Once you logged in with
ssh bandit0@bandit.labs.overthewire.org -p 2220
There is a file called readme in the directory you are in 
which contains the password for the next level. Get
a hold of those contents.


Background
----------


Solution
--------

Requirements: 
- Established connection as bandit0

```sh
# display current working directory
bandit0@bandit:~$ pwd
/home/bandit0

# list contents of a directory
bandit0@bandit:~$ ls
readme

# display the contents of readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```


