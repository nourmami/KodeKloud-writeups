# KodeKoud Architecture


![alt text](https://github.com/nourmami/KodeKloud-writeups/blob/master/kodekloud/0.png "image 1")



## challenge 1

`Question` :  During the daily standup, it was pointed out that the timezone across Nautilus Application Servers in Stratos Datacenter doesn't match with that of the local datacenter's timezone, which is Africa/Akra. 

```shell

    #ssh to tony app01
    ssh tony@stapp01
    
    #check current time zone
    timedatectl
    ls -l /etc/localtime

    #set time zone
    sudo timedatectl set-timezones Africa/Dakar

    #we have to do this in all app servers stapp01,stapp02, stapp03

```
![alt text](https://github.com/nourmami/KodeKloud-writeups/blob/master/kodekloud/1.png "image 1")
![alt text](https://github.com/nourmami/KodeKloud-writeups/blob/master/kodekloud/11.png "image 1")

## Challenge 2

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
![alt text](https://github.com/nourmami/KodeKloud-writeups/blob/master/kodekloud/2-2.png "image 2")




