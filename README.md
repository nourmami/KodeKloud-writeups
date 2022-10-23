#KodeKoud Architecture



## Challenge 1

`Question` :  The System admin team of xFusionCorp Industries has installed a backup agent tool on all app servers. As per the tool's requirements they need to create a user with a non-interactive shell.Therefore, create a user named siva with a non-interactive shell in the app02 server
```shell
    #ssh to steve app02
    ssh steve@stapp02
    
    #switch to root without entering root passwd.
    sudo su -

    #add auser with a non-interactive shell 
    adduser siva -s /sbin/nologin

    #check configuration
    id siva
    cat /etc/passwd | grep siva

```
![alt text](https://github.com/nourmami/KodeKloud-writeups/blob/master/kodekloud/2-2.png "image 1")

