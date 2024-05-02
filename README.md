
# Docker




## FAQ

#### Why Docker is needed ??

-> You may have oftenly heared that it works on my computer but not working on your computer so its your fault !! 

Lets suppose a are woking on a very big project that has huge number of developers working together. Each one working for different portion of project on their pc/laptop that has different configuration from Each other. Now beacuse of this environment difference there is very high chance that it run on your computer but not on others computer beacuse of the version or the environment difference. To overcome this problem without Docker we have to manually replicate the entire environment to other pc. With Docker this problem becomes very easy to tackle.

#### How does Docker solve this problem??

-> It uses the concept of  **Container**. Container is light weight, easy to build and share among different members.

-> Basically whatever the operating systems or tools we are using along with their version it is intergrated within the Container, so no matter what version or os you are using it create its own environment and run the application.

-> Each Container has its own tools, configuration and os. 

#### Difference btw Docker Desktop and Daemon ??

-> Desktop is a command line interface where we can easily interact with the docker. 

-> Daemon is an actual tool that does all the docker job including pushing and pulling an image. interacting with command line, etc.

#### What is Docker Hub ??
 
-> Docker Hub is just like github where it containes the public images which we can pull and run in our computer just like we pull the repository from the github.


#### Image vs Container : 

-> **Image** : In Docker an image serves as an self sufficient software bundle that's capable of running a designated application or service. It encompasses the application code, runtime settings, essential system libraries, dependencies and other required files, for operation

-> **Container**  :  A Docker container is similar, to an portable package that contains all the essentials for an application to function seamlessly. It consists of the application as the necessary tools and configurations. These containers operate autonomously on your device with each containers data being separate, from that of others.


#### Does Docker have caching functionality??

-> Docker has caching functionality this means that once you build your container and run the image firstly it search locally and if not found for the first time then it will store it in the cache so next time when you again try to run the image it will run faster as compare to the previous one.
## Port Mapping & Environment Variables

Why Port Mapping is necessary??

-> let suppose u have define a port inside your image let say 8000. Now when you run this image in an container the container will have run this app on this port number.But since we know that the container is isolated from outside environment so this port number would be invalid or it not working  so we have to do the port making

The command for port Mapping is :

**docker -p 8000:8000 'image_name'**

here -p stands for the port mapping.

-> You can also change the port number on your local host but you cannot change the port number inside the container.

For eg : **docker -p 6000:8000 'image_name'**

When you run this it will say 'server running on 8000' but to access it you have to do "local/host:6000" on your browser.


-------------------------------------------------------------------

You can pass environment Variables like : 

**docker -p 6000:8000 -e key=value 'image_name'**

where -e stands for environment Variables

-> It is necessary when you want to pass some info to the container from outside environment.
