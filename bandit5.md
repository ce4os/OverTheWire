Bandit Level 4 - Filetype investigation
=======================================


Goal
----

Get a hold of password for bandit5. 
The password is stored in the only
human readable file in the inhere/
directory. 


Background
----------


Solution
--------

```sh
## Solution 1 - Verbose
bandit4@bandit:~$ ls 
inhere
bandit4@bandit:~$ ls inhere/
-file00  -file02  -file04  -file06  -file08
-file01  -file03  -file05  -file07  -file09
bandit4@bandit:~$ file inhere/-file00
inhere/-file00: data

bandit4@bandit:~$ file inhere/-file02
inhere/-file02: data

bandit4@bandit:~$ file inhere/-file03
inhere/-file03: data
...
bandit4@bandit:~$ file inhere/-file07
inhere/-file07: ASCII text

bandit4@bandit:~$ cat inhere/-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR


## Solution 2 - using wildcard *
# Using the wildcard * allows you to investigate all files in one go
bandit4@bandit:~$ file inhere/*
inhere/-file00: data
inhere/-file01: data
inhere/-file02: data
inhere/-file03: data
inhere/-file04: data
inhere/-file05: data
inhere/-file06: data
inhere/-file07: ASCII text
inhere/-file08: data
inhere/-file09: data

bandit4@bandit:~$ cat inhere/-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```

