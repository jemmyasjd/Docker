
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
