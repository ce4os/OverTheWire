# Walkthroughs for wargames hosted at overthetwire.org

The wargames offered at this site teach the basics of terminal usage [bandit],
webserver security[natas], cryptography[krypton] and many other security related
topics. Make sure to visit [OverTheWire](https://overthewire.org/wargames/)!

Although there are already a great many of solutions out there, I decided 
to write down my own solutions. 
For future reference, documentation and to practice duckdebugging. 

If you are searching for solutions because you are stuck at level XY I strongly
recommend that you give yourself some time before checking the solution someone
else came up with. Sometimes a little distance, a walk, some distraction does the
trick and you will be able to solve a problem. 

[SPOILER ALERT]

For convenience I created a config file in the .ssh/  directory in my home folder so
I can easily access and login to the different levels. 
The config file looks sth. like:
```config
Host banditlabs
	HostName bandit.labs.overthewire.org
	Port 2220
```
banditlabs is an arbitrary name you can change according to your liking. 
The rest is mandatory. I did this because
```sh
ssh bandit0@banditlabs
```
is more comfortable to write than 
```
ssh bandit0@bandit.labs.overthewire.org -p2220
```

Have fun!!!
