## Introduction to Linux and the Linux Command Line

CPSC 2810



### Introduction Questions

Who knows which firewalls we have by default on Ubuntu?


### Introduction Questions

Who has used UFW before?


### Introduction Questions

What is the difference between the inbound and outbound rule chains?



## Explore

* Get into pairs
* Add a firewall rule that blocks incoming http traffic
* Try accessing the website at your ip address? What happens and why?
* Delete the rule blocking http
* Set the default outbound policy to Deny. What practical effect does this have?

Note: Make sure students have a desktop install of Ubuntu



## UFW Basics


### UFW = Uncomplicated FireWall


### UFW Basics: Syntax

View the current ruleset

```
sudo ufw status verbose
```

This shows the current logging level, chain defaults, and the active ruleset.






