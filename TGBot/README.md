# TGBot Dockerfile


This docker file runs a bot for telegram written in nodejs. 
Github link for original bot: https://github.com/jmendeth/node-botgram.git

### Reasons for this Dockerfile:
--------------------------------
This bot runs directly in the system, so it might be unsafe if used in group chats because of abuses it might get.  
I was in need of linux access in telegram groups, so running this bot on top of alpine linux container was a great solution.  


### Usage:
---------
1. Create a bot with botfather
2. Get auth token of the bot from botfather
3. Get your telegram ID or Group ID 
4. Build this docker file and supply the Auth_token and ID when starting the container
5. More information on creating bot from botfather, Auth_Token, ID etc can be found in various telegram bot tutorials, make sure to go through them.


**Example:**
* To build:  
`docker build -t tgbot .`

* To run:  
`docker run --name tgbot_container tgbot 00000:000000000000000000 123456787`

* Note:
- If you want to have bot AuthToken and ID by default then you can edit the commented part in the Dockerfile at the end. Remember, this should be done only if you are sure that the dockerfile won't go into the wrong hands as your bot might be abused. Anyways, in that case you can change the AuthToken of your bot via botfather.  

*For more information about the bot please check the github repo mentioned earlier.*


