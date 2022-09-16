### <u>**Instructions to build the docker images and containers**</u> 

I use the docker image from Jonas Vautherin. In his GitHub there are the Dockerfile, entry point and so that allows us to re build and modify the original images. But I had tried to do the modification but there is a problem with the base image for Ubuntu:18.04. Therefore it is possible to build the image with the Jonas image saved in the dockerhub.

First of all, do you need to install docker service in your computer (if do you prefer docker desktop is well)

In your terminal execute the next line:

**docker run --rm -it --env PX4_HOME_LAT=47.397742 --env PX4_HOME_LON=8.545594 --env PX4_HOME_ALT=488.0 jonasvautherin/px4-gazebo-headless:v1.13.0**

The next 3 are environment variables to change the home position in **QGroundControl**. You can put the position in the world that you want.

**PX4_HOME_LAT=47.397742** 

**PX4_HOME_LON=8.545594** 

**PX4_HOME_ALT=488.0**

In the next step is necessary to run the mavsdk_server (for the platform you use). In the .zip file is attached the mavsdk_server for windows (also you can download it from the web) 



### <u>**Steps for Python setup**</u>

Python 3.6+ is required (because the wrapper is based on [asyncio](https://docs.python.org/3.7/library/asyncio.html)).

To install mavsdk-python, simply run:

**pip3 install mavsdk**



