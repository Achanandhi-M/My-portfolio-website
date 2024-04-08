---
title: "Docker🐬 Dreams💭-3"
description: "Docker for Begineer Series"
dateString: July 2023
draft: false
tags: ["Contanier","Devops","Docker","DockerHub", "Linux","Nginx","tech"]
weight: 109
cover:
    image: "/blogs/dockerpng.png"
---

Hi friends🙋‍♂️ welcome back to Blogs-with-Achu, we have started the Docker🐬 Learning series, In my previous Blog⏮️ we saw about **_web servers and also a practical demonstration of running a web server inside a docker container._**

**Today's Quote:**

> # _"Service to others is the rent you pay for your room here on earth🌎"_
> 
> ## **\- Muhammad Ali**❤️‍🩹

**Today's Exciting Blog Agenda:**

1. **what is Dockerfile?**❓

3. **Why Dockerfile Matters! 🤔**

5. **Launch Your Website with Nginx and Dockerfile! ⛵️🚀**

7. **What's Next in our Docker Journey?🌈🚀**

9. **Conclusion🏁**

**1) What is Dockerfile**❓

_According to the Docker doc,_

Docker can build🏗️ images automatically by reading the instructions from a `Dockerfile`. A `Dockerfile` is a text document that contains all the commands a user could call on the command line to assemble an image. I think it may sound like complicating let me explain in a simple diagram✍🏻

![](/my-demo-portfolio/static/blogs/blog-1.jpg)


Don't get confused😕 whiling seeing the diagram, it is just a simple illustration we often experience when we visit the hotel. Let's compare this with Dockerfile creation and Execution. How the user is giving an order to the waiter, so like as the same, the user creates Dockerfile in their system, and how the waiter gives the order to the chef for preparing the food the user is given, same likewise the Dockerfile instructs the Docker to create the image based on the command mentioned by the user, after the chef Finished cooking the waiter serves the food to the user, same like in Docker🐬 world, the Docker Engine builds the container based on the Image built in the previous step.

_**Remember the Dockerfile does not contain any file Extension**_

Let's Compare the above example with this example

![](/my-demo-portfolio/static/blogs/docker-new-1.jpg)

I think the above example clearly explains the role of Dockerfile, In the Dockerfile u mention all of your stuff like Dependencies and libraries in the form of Commands. Apart from that, we can include environment variables in Dockerfile.

In summary, a Dockerfile is like a recipe that instructs Docker🐬 on how to build a Docker image, which is a self-contained package containing all the necessary ingredients (dependencies) and instructions to run your application in a consistent and portable manner, just like a well-prepared dish you order in a hotel. Dockerfile makes creating and sharing these recipes easy, allowing others to enjoy the same delicious meal (application) in their own containers.

2) **Why Dockerfile Matters! 🤔**

Dockerfile matters because it defines the steps to create Docker images, ensuring reproducibility, version control, simplified deployment, isolation, and scalability for containerized applications.

3) **Launch Your Website with Nginx and Dockerfile! ⛵️🚀**

Let's see a practical demo, we are going to see the same example as we saw in our previous blog, but the difference is that we are not going to manually go to deploy this, we are doing by this creating a very very simple Dockerfile

Follow the below steps below to do

```
mkdir nginx-demo-Blog #create separate Directory
cd nginx-demo-Blog
vi Dockerfile # Create Separate Dockerfile
vi myWebPage.html #Create html file
```

![](/my-demo-portfolio/static/blogs/nginx-1.png)

I think the above Dockerfile📁 is very simple because it will not contain that many commands in Dockerfile, Dockerfile contain only Two commands FROM and COPY commands, FROM Command, is used to mention the base image which we are going to use in our later part, and the COPY command is used to COPY the files to a directory inside the container. We will see more commands and complex Dockerfile in a later blog.

_This is our HTML file \[myWebPage.html\] or you can use your own Html file please feel to modify_

![](/my-demo-portfolio/static/blogs/nginx-2.png)

```
docker build -t[tag] <image-name>

docker build -t nginx:alpine .
```

![](/my-demo-portfolio/static/blogs/nginx-3-1.png)

Remember ⚠️to include "." at the end of the docker build command, When you run the `docker build` command with the "`.`" (dot) at the end, it tells Docker to search for the Dockerfile in the current directory. Docker will use all the files and directories in the current directory as the build context

The docker build command is used to build our Docker image based on the instructions we mentioned in our Docker file. The output shows the image is built successfully.

Again, We need to cover a lot about Image layers, which is one of the important concepts in the Dockerfile concepts, we focus a lot more in the next blog.

```
docker images
```

Use the docker images command to verify the image present in our system.

![](/my-demo-portfolio/static/blogs/nginx-5-1.png)

We successfully 🚀💪built our image by ourselves using our own Dockerfile, We need to create a container for our image using this command

```
docker run [options] <container-name> <image-name>

docker run -d -p 84:80 nginx-webpage nginx-alpine
```

![](/my-demo-portfolio/static/blogs/nginx-6.png)

The -p command is used to expose what we saw in our previous blog, I think we need to ask ourselves what these numbers denote 84:80 ?? 84 is the port number of the host side which we enter in the browser along with the Ip address , 80 port number denote the container port

**How we can make sure that we deployed successfully**❓😕

Use this command

```
docker exec -it nginx-webpage sh
```

![](/my-demo-portfolio/static/blogs/nginx-7.jpg)

The above output shows we deployed in the correct directory

**_Our Output Looks like this:_**

```
http://yourIpAddress:portNumber/fileName
```

![](/my-demo-portfolio/static/blogs/output-1.png)

If you got this output 😂😅 Yeah we Successfully deployed our web page into the Nginx web server using Dockerfile, If your creating your own web page make sure that you got correct the output, if not please mention it the in comments section

**What's Next in our Docker Journey?🌈🚀**

In our next blog, we can deep delve into docker concepts and also we can see some more examples.

**Conclusion**🏁

If you have any doubts, please mention them in the comment section. Let's keep up the enthusiasm and explore the real power of Docker in our upcoming blog. See you in the next blog. Happy learning and happy reading! 📖

Regards

Achanandhi M👦
