Bandit Level 8 - Grep that password 
===================================

[Level 8](https://overthewire.org/wargames/bandit/bandit8.html)

Goal
----

The password for the next level is stored in the file data.txt next to the word millionth

Solution
--------

bandit7@bandit:~$ cat data.txt | grep millionth
millionth	TESKZC0XvTetK0S9xNwm25STk5iWrBvP


Bullet Points:
--------------

grep
pipes
