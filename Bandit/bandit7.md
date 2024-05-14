Bandit Level 7 - Find that file
===============================

[Level 7](https://overthewire.org/wargames/bandit/bandit7.html)

Goal
----

The password for the next level is stored somewhere on the server and has all of the following properties:

    owned by user bandit7
    owned by group bandit6
    33 bytes in size


Solution
--------

```sh
# Search from root of FS on for a file which is owned by group 
# bandit6, owned by user bandit7 and is 33bytes of size
# leads to a lengthy list of Error messages: Permission denied.
# You can scroll through and will finally find the respective file

bandit6@bandit:~$ find / -type f -group bandit6 -user bandit7 -size 33c
find: ‘/etc/ssl/private’: Permission denied
...
/var/lib/dpkg/info/bandit7.password
...
find: ‘/run/lock/lvm’: Permission denied

bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password 
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

# This is rather ugly. Imagine if the list would be one million entries long. 
# This would be a needle in a haystack kind of problem.
# But there is a more elegant solution for this problem. 
# Redirect all error messages to device 0
bandit6@bandit:~$ find / -type f -group bandit6 -user bandit7 -size 33c 2>/dev/null
```

Bullet Points:
--------------

Device Null
Redirecting Errors
find

