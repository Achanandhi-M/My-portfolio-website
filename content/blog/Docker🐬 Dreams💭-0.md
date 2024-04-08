---
title: "Docker🐬 Dreams💭-0"
description: "Docker for Begineer Series"
dateString: July 2023
draft: false
tags: ["Contanier","Devops","Docker","DockerHub","tech"]
weight: 112
cover:
    image: "/blogs/dockerpng.png"
---


Hi friends, welcome back to Blogs-with-Achu, we have started the Docker🐬 Learning series, In my previous Blog⏮️ we saw Introduction to Docker and containers, Today in this blog we are Going to see Docker installation and working with some basic Docker commands.

**Today blog's is all about :**

- Docker Installation🏠

- Docker Desktop💻

- Alternative method-Sandbox☁️

- Check Docker is Installed🫡

- Basic Docker Commands💥

- What's Next⏭️

- Quiz🧾

- Conclusion.🏁

**Docker Installation**🏠..

For working with docker, we need to first install docker in our local system💻. The installation process will defer based on the operating system.

Step 1: Use this Link [docker.io](https://www.docker.com/) for installation

![](/my-demo-portfolio/static/blogs/docker-06.png)

Step 2: After that, u will land in the Docker world

![](/my-demo-portfolio/static/blogs/docker-5.png)

Step 3: Install Docker based on your operating system, if you're using Linux install based on your Linux distributions

I think the Installation process is easy, I hope you have done that. If are facing any issues please mention them in the comment section.

**Docker Desktop💻  
**Docker Desktop is a tool designed to simplify the development and deployment of containerized applications. It provides an easy-to-use graphical interface for managing Docker containers and images on your local machine, regardless of the operating system you're using.

**_Alternative method-Sandbox_**☁️

There is another alternative method, you can run docker without installing it in your local system, yes you heard that right. Yeah, you can run docker in the cloud (that's like in a sandbox environment). They are many websites are providing a sandbox environment for absolutely free, you can use it.

Use this link for [Docker's official sandbox Environment](https://www.docker.com/play-with-docker/)

![](/my-demo-portfolio/static/blogs/docker-07.png)

There are many websites providing sandbox environments you can also try the [codesandbox.io website](https://codesandbox.io/docs/tutorial/getting-started-with-docker)

**_Problem with Sandbox Environment_**😵‍💫

There are Several problems are there while working with a sandbox environment

1. **_Resource Limitations_**: Docker imposes resource limits on containers to ensure fair sharing of resources with the host system and other containers. However, these limits can sometimes restrict the sandbox environment's capabilities, such as memory, CPU, or network access.

3. **_Container Lifecycle and Persistence_**: By default, Docker containers are ephemeral, meaning any changes made inside the container are lost when it's stopped or restarted. This can be problematic when working with a sandbox environment that requires persistence.

5. **_Debugging and Troubleshooting_**: Debugging issues within a Docker sandbox environment can be more challenging due to the isolation.

The sandbox environment is best suitable for testing purposes, it is not suitable for individuals who want to play hard with the docker

**Check Docker is Installed**🫡

If you installed docker locally on your system, you are already one foot ahead of learning docker, there are several way use can verify whether you installed docker in your local machine. Use this command to verify :

```
docker --version
```

![](/my-demo-portfolio/static/blogs/docker-image.png)

I am running docker inside Ubuntu, and it shows the current version of docker installed on your local machine.

**Basic Docker Commands**💥

There are some basic docker commands you can use frequently when working with docker

1\. docker images command will display all images in our local system

```
docker images
```

The lists of docker images in my local system.

![](/my-demo-portfolio/static/blogs/docker1.jpg)

2\. docker container ps -a command will display all container both excited and running.

```
docker container ps -a
```

![](/my-demo-portfolio/static/blogs/docker-4.jpg)

3\. docker container ps command will display the container which are running

```
docker ps
```

![](/my-demo-portfolio/static/blogs/docker-3-1.jpg)

In the above image, there is no container running in my local system, so it shows nothing.

**What's Next**⏭️

In the next blog, we deep dive into the docker images concept, how to pull images from the docker hub, and how to work with images and containers with examples.

**Quiz**🧾

**Conclusion**🏁

If you have any doubts, please mention them in the comment section. Let's keep up the enthusiasm and explore the real power of Docker in our upcoming blog. See you in the next blog. Happy learning and happy reading! 📖

Regards

Achanandhi M👦
