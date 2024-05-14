Bandit Level 9 - uniq does the trick
====================================

[Level 9](https://overthewire.org/wargames/bandit/bandit9.html)

Goal
----

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

Solution
--------

bandit8@bandit:~$ file data.txt 
data.txt: ASCII text
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t

Explanation
-----------

File data.txt only contains ASCII characters. There is only one line that is uniq the rest repeat.
If you run 
cat data.txt | uniq -u 
you will get uniq strings but not the uniq string. You need to sort the contents first and than pipe
it into uniq. This seems a bit like using aggregate functions in sql. 



Bullet Points:
--------------

ASCII 
sort
uniq

