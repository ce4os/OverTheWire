Bandit Level 4 - Hidden files
==============================

[Level 4](https://overthewire.org/wargames/bandit/bandit4.html)

Goal
----

Get a hold of password for bandit4. 
The password is stored in a hidden 
file in the inhere directory. 


Background
----------


Solution
--------

```sh
## Verbose solution
# Print working directory
bandit3@bandit:~$ pwd
/home/bandit3

# List visible contents of directory
bandit3@bandit:~$ ls
inhere

# Change directory to inhere/
bandit3@bandit:~$ cd inhere/

# Print working directory
bandit3@bandit:~/inhere$ pwd
/home/bandit3/inhere

# List all contents of inhere/ in human readable format
bandit3@bandit:~/inhere$ ls -lah
total 12K
drwxr-xr-x 2 root    root    4.0K Oct  5  2023 .
drwxr-xr-x 3 root    root    4.0K Oct  5  2023 ..
-rw-r----- 1 bandit4 bandit3   33 Oct  5  2023 .hidden

# Display contents of .hidden
bandit3@bandit:~/inhere$ cat .hidden 
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

# Solution 2: Short version
bandit3@bandit:~$ cat inhere/.hidden 
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```

