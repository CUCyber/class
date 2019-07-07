## Cybersecurity Competition Training

CPSC 4810



### Introduction Questions

* Who has used SSH?
  * What client do you use?



### Introduction Questions

* Who has used FTP?
  * What client did you use?



### Explore

1. Get into groups of 2
2. Get credentials from instructor
2. FTP
  * Get a file
  * Upload a file
3. SSH
  * Get process listing of remote machine
4. SCP
  * Get a file
  * Upload a file



## FTP Misconfigurations



### FTP Anonymous Login

/etc/vsftpd.conf

```
anonymous_enable=YES
anon_root=<PATH>
no_anon_password=YES
```

Note:
* Ask "What does anonymous login mean?"
* Explain



### FTP Root Directory

/etc/vsftpd.conf

```
local_root=/
```

Note:
* What's wrong with sharing your root directory?
* How could someone get your passwords if they can upload and download from your filesystem?



### SSH Private Keys

* SSH key data is stored in `~/.ssh`
* id_rsa vs id_rsa.pub
* authorized_keys

Note:
* Always need to check keys to see who can access the machine
* Red teams like to backdoor by adding their keys



### SSH PermitRootLogin

`/etc/ssh/sshd_config`

```
PermitRootLogin yes/no/without-password
```

Note:
* without-password option means you can only log in with private keys
* You may want to change this to `no` if you have console access just to be safe



### SSH PermitEmptyPasswords

`/etc/ssh/sshd_config`

```
PermitEmptyPasswords yes/no
```

Note:
* Doesn't let people log in with empty passwords
* Just useful in case



### SSH AllowUsers

`/etc/ssh/sshd_config`

```
AllowUsers root max weston
```

Note:
* Allows users root, max, and weston to log in



### Questions?