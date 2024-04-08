---
title: "Docker🐬 Dreams💭-2"
description: "Docker for Begineer Series"
dateString: July 2023
draft: false
tags: ["Contanier","Devops","Docker","DockerHub","tech","webserver","Nginx"]
weight: 110
cover:
    image: "/blogs/dockerpng.png"
---

Hi friends🙋‍♂️ welcome back to Blogs-with-Achu, we have started the Docker🐬 Learning series, In my previous Blog⏮️ we saw about **_docker images and containers with real examples_**.

**Today's Exciting Blog Agenda:**

1. **Web Servers: Your Website's Backbone!**🦴

3. **Running a Web Server Inside a Container**🐬

5. **Exposing Your Website to the World! 🌐**

7. **What's Next in our Docker Journey?🌈🚀**

9. **Conclusion**🏁

1) **Web Servers: Your Website's Backbone!**🦴

Before we delve into web servers, we first need to understand what is the server? Don't get overwhelmed😵 when you hear the term server, see basically server is a computer💻 only, the server has high computing power and memory resource than our normal machines. Our normal computer is designed for small use cases, but servers are meant for high-performing tasks💪. The main purpose of the server is to provide service, Hmm.....what kind of service?🤔 The service depends on the use case if the server belongs to a web server, then the server serves websites, if the server belongs to a file server like FTP, it stores and manages files related to the client, if the server belongs to email server then it belongs to provides service related email, so they are many servers, the main goals of these servers is to provide service to the user with zero downtime.

In **Simple terms**,

**Server**: A computer or system that provides services or resources to other computers or devices on a network.

**Web Server**: A specialized server that stores and delivers website files to users' web browsers when they access a website on the internet.

**Problems with physical data centers servers**

But when we are talking about servers, we need to consider one important factor maintenance, Maintenance ? for what? For server only, Server is like our computer, But It is a big computer, and it needs to run continuously 24X7 for providing service to the user, Thing in the way if my server is running 24X7 it needs a continuous power supply, a separate person to monitor the performance of the server if my server is down or crashed my user will not get the service, so separate person needs to monitor the health of the user, Now we are dealing with a single server, but what happens when our user is increased?⬆️ our single server is not able to handle the request from a user, so we need an additional server when our user base is increasing. See on the flip side we purchased 100 servers due to an increase in userbase, what happens when unfortunately the userbase is decreased, our 100 purchased server is a waste, our purchasing cost is a waste, and our human resources is a waste in this situation.

Only one solution for the above problem is to migrate to the cloud,☁️ It will take care of you. Again this is a separate topic we will cover in another blog, I have already written blogs related to the cloud, if you want to know check it out.

**Running a Web Server Inside a Container**🏃‍♂️

Now we focus on how to run our web server in our docker container. One thing I want to mention here is that you don't need to purchase any server or don't want to set up any server in the cloud or on-premises for this example, because we are testing in our local system as a local host, running our web server locally does not require any requirements, you just need to install web server like Apache or Nginx, these two web servers are most popular and both are open source.

In our previous example, we ran hello world using hello-world docker image, the same methodology here, first, we need to pull the image and we want to run the container using that image, and finally, we want to expose the container that's all.

Let's start by identifying our end goals, what is our end goal guys? we need to run a web server inside a docker container, so we need to pull the image related to a web server in this case either Apache or Nginx, you can choose either one based on your use case. For this example, we use Nginx as our web server.

**Use this command to pull the Nginx web server**

```
docker pull nginx
```

![](/my-demo-portfolio/static/blogs/img-1.png)

we have successfully pulled the nginx image from the Docker hub, Next check it once we have that image by typing the command

```
docker images
```

![](/my-demo-portfolio/static/blogs/img-2.png)

Next we have create an isolated environment (container) for running our Nginx image By using the command

```
docker run -d -p 80:80 --name nginx-container nginx
```

![](/my-demo-portfolio/static/blogs/img-11.png)

Here --d flag is used for running a container in a detached mode which means running in the background, --name flag is used to name a container, we can give any name to a container, but remember two containers should not have the same container. The -p flag which I will mention in later part of this section.

Next, we have to deploy our web page to the nginx web server, there are two ways we can do it, one by the manual method that is we deploy our webpage in the nginx directory, and another one is my favorite method is by automating the deployment process while building the docker image itself by using Dockerfile. But now in this, we see the first method and the second we will see on Next blog.

There is a separate command to enter into the docker container, the directory that is also present inside the docker container.

```
docker exec -it nginx-container sh
```

Here exec is a Docker sub-command that allows you to run a command inside a running container, -it these are options used together to make the execution interactive. The "-i" option enables interactive mode, and the "-t" option allocates a pseudo-tty, which provides a terminal-like interface for interaction, nginx-container is the name of the container and finally sh is command we want to run inside the container. In this case, we are specifying "sh," which starts an interactive shell session in the container.

**Here is the directory path where we want to deploy our webpage: /usr/share/nginx/html**

![](/my-demo-portfolio/static/blogs/img-4.png)

We are now inside the docker container, the shell session is open inside the docker container, and we need to deploy our webpage inside the directory which I mentioned in above.

![](/my-demo-portfolio/static/blogs/img-5.png)

We are now inside the directory, we need to deploy our webpage in this directory, we need something called a text editor because if are manually deploying means we need a text editor for coding and deploying in that directory, I use Vim use can also use emacs or nano other as well as.

```
apt-get update #for updating the installed packages
apt install vim #for installing vim text editor
vim hello.html #you can give any name for your html file
```

vim is a command used to open the Vim text editor following our file name.

![](/my-demo-portfolio/static/blogs/img-7.png)

![](/my-demo-portfolio/static/blogs/img-8.png)

Once u typed vi hello.html the blank page will open you can write your code in that and once you finished press the ESC button and type wq for saving your file.

![](/my-demo-portfolio/static/blogs/img-9.png)

Once finished we can check by typing ls command

![](/my-demo-portfolio/static/blogs/img-10-1.png)

Boom, We successfully deployed our webpage inside the nginx web server which is running in a docker container. By default the docker container is not accessible outside the docker network, then how we can access our web page deployed in the Nginx web server?

**Exposing Your Website to the World! 🌐**

```
docker run -d --name -p 80:80 nginx-container nginx
```

we previously used this command for creating an instance of our image, there I didn't mention the -p flag, I think it is the correct place to explain. If you want to make a Docker container accessible from outside the Docker network, you need to explicitly publish the container's ports to the host system using the `-p` option when running the container. This process is known as port mapping or port forwarding. By doing this, you can access the exposed ports of the container through the host system's IP address or hostname. That why we need -p to mention in the command.

```
http://yourHostIpaddress/yourFileName
http://192.168.174.128/hello.html
```

![](/my-demo-portfolio/static/blogs/output.png)

Wow, We have done it congratulations we have successfully deployed and accessed our webpage. If you got it error like "This site can’t be reached" we accessing, sorry you made a mistake, please cross-check it, surely u will get it. If you are struck and getting error means , please free to mention it in a comment section , I will surely help you.

**What's Next in our Docker Journey?🌈🚀**

In our next blog, we can see the same example by automating the deployment process by using Dockerfile.

**Conclusion**🏁

If you have any doubts, please mention them in the comment section. Let's keep up the enthusiasm and explore the real power of Docker in our upcoming blog. See you in the next blog. Happy learning and happy reading! 📖

Regards

Achanandhi M👦
