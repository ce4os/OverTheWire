Bandit Level 10 - Getting rid of that code
===========================================

[Level 10](https://overthewire.org/wargames/bandit/bandit10.html)

Goal
----

The password for the next level is stored in the file data.txt in one of the few human-readable strings, 
preceded by several ‘=’ characters.

Solution
--------

bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ file data.txt 
data.txt: data
bandit9@bandit:~$ cat data.txt | strings | grep =========
x]T========== theG)"
========== passwordk^
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s


Bullet Points:
--------------

strings
