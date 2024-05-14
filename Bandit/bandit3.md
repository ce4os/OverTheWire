Bandit Level 3 - Autocompletion to the rescue 
=============================================

[Level 3](https://overthewire.org/wargames/bandit/bandit3.html)

Goal
----

Get a hold of password for bandit3. 
The password is stored in a file named
spaces in this filename


Background
----------

In Linux, you can choose basically every filename you want. 
While this grants a certain amount of freedom, it can lead
to problems too. 

Solution
--------

```sh

## Solution 1: Manual typing
# The backslash character can often be used as an escape character for 
# characters with special meaning in this case the space character
cat spaces\ in\ this\ filename

## Solution 2: utilizing autocompletion
# using autocompletion: type in cat and press tab two times
bandit2@bandit:~$ cat 
.bash_logout             .profile                 
.bashrc                  spaces in this filename  
# now add a s and press tab
cat spaces\ in\ this\ filename 
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
