#Radicale Dockerfile
---
This docker file builds an image for Radicale with alpine linux as base.  
To know more about what Radicale is go [here](http://radicale.org)

#Usage:
---
### 1. Build image

`docker build -t radicale .`

### 2. To run:

`docker run -dit --name radicale -p 5432:5432 radicale`

### 3. Basic Radicale Usage

I used to use Baikal for my cal/carDAV. Not sure why but I was not satisfied with it. So was searching for something similar but more lightweight and easier to setup and came across radicale. I didn't want Radicale to run in my main system so created a Docker container that hosts my contacts and calendars (mostly contacts).  

For android you can get DAVDroid for free from Fdroid. And for Linux I used Kontact (Don't use much).

*For more info about radicale and its uses please check the link mentioned earlier*
