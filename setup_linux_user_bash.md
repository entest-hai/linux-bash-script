# Setup Linux User and Bash 
**Hai Tran 25 APR 2022**

### linux shell 
- /usr/bin/bash 
- /usr/bin/csh

### username and hostname  
bash shell it look like this 
```
username@hostname:~$ 
```
cshell it look like this 
```
(base)[username@localhost ~]$ 
```

### edit username and hostname in ~/.bashrc 
to have this format username@hostname:~$ 
```
vim ~/.bashrc
```
and 
```
PS1="\u@\H:\w\$ "
```
to have this format username:~$
```
PS1="\u:\w\$ "
```