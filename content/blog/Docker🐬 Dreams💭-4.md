---
title: "Docker🐬 Dreams💭-4"
description: "Docker for Begineer Series"
dateString: September 2023
draft: false
tags: ["Contanier","Devops","Docker","DockerHub","tech"]
weight: 104
cover:
    image: "/blogs/docker-4.jpeg"
---


Hi friends🙋‍♂️ welcome back to Blogs-with-Achu. This blog is the continuation of our Docker Dreams learning series. We learned a little about containers and docker in our previous docker-related blogs. Today we will see about Docker Hub_(a place where we store our images)._

**In this Blog:**

- **What is Docker Hub? Why do we need it**❓**🤔**

- **How to publish your own image to Docker Hub**❓**🤔**

- **Demo part ⛵️🚀**

- **What next?🌈🚀**

- **Summary**🏁

**What is Docker Hub? Why do we need it**❓

Docker hub serves as a repository where developers can store, share, and distribute container images. we already know about the container images which contain everything needed to run a piece of software, including the code, runtime, libraries, and system tools. Docker Hub provides a central location for developers to find and use pre-built container images, streamlining the process of packaging and deploying applications in containers.

Docker Hub is a concept more likely related to GitHub. we use GitHub for project collaboration with multiple developers who are working on the projects. The same concepts are used here we are using Docker Hub for storing our container images, and GitHub for storing our code. In both concepts, we can use the version control method.

**How to publish your own image to Docker Hub**❓**🤔**

Publishing our images to Docker Hub is not rocket science, we can easily push our image to Docker Hub in just two commands. Before publishing, we need to create an account in Docker Hub.

If you don't have an account use think link https://hub.docker.com/signup to signup

![](/my-demo-portfolio/static/blogs/dockerhub-home.png)

**Once you created an account, it some how look like this**

![](/my-demo-portfolio/static/blogs/dockerhub-home-2.png)

**Once you log in you don't see any repository, but in the above image, there are two images are there which were created by myself.**

**_Note:_**⚠️

_Docker Hub offers two kinds of service community edition and pro edition, the difference between them is in the Pro edition we have the option_ to store our images privately, but in the community edition, we also have the option to store one image private, we need to store our image public in the _community edition. Choose the option based on your use case._

**Demo part ⛵️🚀**

I think we have seen enough theory, it's time to get our hands dirty.

```
sudo docker  images #use to list the images
```

![](/my-demo-portfolio/static/blogs/terminal.png)

You can also build your own application in the image and push that image into Docker Hub, and once it is uploaded anyone can pull it and use it on their own local machine. I am using my own image for the demo part

```
docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]
sudo docker tag nginx:alpine achanandhi/nginx:alpine
```

Before pushing the image into the docker hub you need to tag the image.

![](/my-demo-portfolio/static/blogs/terminal-1.png)

```
sudo docker login #login into docker hub
```

Once you enter the command it will ask you to enter the credentials (email id and password) once you enter the credentials it will log in successfully, the output somewhat looks like this:

![](/my-demo-portfolio/static/blogs/terminal-02.png)

```
sudo docker push  achanandhi/nginx:alpine
```

Once you enter the command, it will push your image from the local computer into the docker hub repository.

![](/my-demo-portfolio/static/blogs/terminal-03.png)

Boom.. we successfully pushed our image, let's see in the Docker hub repository

![](/my-demo-portfolio/static/blogs/dockerhub-home-3.png)

Our docker image is successfully uploaded into the docker hub.

**What next?🌈🚀**

Our next target is focusing on cloud providers, and how we use the cloud services related to containers(ECS, Google Cloud run Azure Cloud Instances).

**Summary**🏁

If you have any doubts, please mention them in the comment section. Let's keep up the enthusiasm and explore the real power of Docker in our upcoming blog. See you in the next blog. Happy learning and happy reading! 📖

Regards

Achanandhi M👦
