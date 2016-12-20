#Cowrie Dockerfile
---
This docker file builds an image for Cowrie with alpine linux as base.  
To know more about what Cowrie is go [here](http://www.micheloosterhof.com/cowrie/)

#Usage:
---
### 1. Build image

`docker build -t cowrie .`

### 2. To run:

`docker run -dit --name cowrie -p 22:2222 cowrie`

### 3. Notes

This runs a forked version of cowrie. You can check the source [here](http://github.com/avasz/cowrie).  
Changes from original cowrie are listed below:  

1. Accepts more than 86779 usernames with any passwords.  
2. Doesn't use python virtualenv as docker itself is isolation. 
3. Automatically starts to follow the cowrie.log file such that if you attach to the detached docker container you will see the live logs. Use normal docker `exec` arguements if you want to connect to the shell in the container.  

*For more info about cowrie and its uses please check the link mentioned earlier*
