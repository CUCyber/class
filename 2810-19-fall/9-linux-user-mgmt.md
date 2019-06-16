## Introduction to Linux and the Linux Command Line

CPSC 2810



### Introduction Questions

Who knows how to add and remove users on Linux?


### Introduction Questions

Who knows how to change the password for a user?


### Introduction Questions

Why would you want to add a user to a group on Linux?


### Introduction Questions

Who knows how to escalate to admin from their local user on Linux?


### Introduction Questions

Who knows how to create and enforce a password policy on Linux?



## Activity

* Get into pairs
* List all users on the system that begin with the letter "r"
* List all of the groups that the user "ryan" is a part of.
* Add a user named "frederick and set his password to "freder1ck-r0cks"



## Users


### Where does the system store users?


### Where does the system store users?

/etc/passwd

* Username
* User [has = (!)] or [does not have = (\*)] a password
* User ID (UID)
* Group ID (GID)
* Home Directory
* Shell

![](passwd.png)


### Where are the passwords for users stored?

/etc/shadow

* Username
* Encrypted Password
* Days since password was changed
* Days before password can be changed
* Days after which password must be changed
* Days to warn user of expiring password
* Days after expired password that the account is disabled
* Days that an account has been disabled

Note: 
An easy way to check if a user has a password set is to take a peek at the encrypted password field of /etc/shadow

### Adding and Removing Users
