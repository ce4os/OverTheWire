Bandit Level 6 - Find that file
===============================

[Level 6](https://overthewire.org/wargames/bandit/bandit6.html)

Goal
----

Get a hold of password for bandit6. 
The password for the next level is stored in a file somewhere under 
the inhere directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable


Solution
--------

```sh
## Short solution: suppose only one file is of size 1033 and not executable
find inhere/ -size 1033c ! -executable
inhere/maybehere07/.file2
bandit5@bandit:~$ cat inhere/maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

## Short solution: above mentioned condition must not hold true
finding a file that is human readable and find the one with size 1033c and not executable
file inhere/*/* | grep ASCII | find -size 1033c ! -executable 
bandit5@bandit:~$ cat inhere/maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
