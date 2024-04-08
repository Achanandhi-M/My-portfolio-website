---
title: "Docker🐬 Dreams💭"
description: "Docker for Beginner's"
dateString: July 2023
draft: false
tags: ["Contanier","Devops","Docker","DockerHub","tech"]
weight: 113
cover:
    image: "/blogs/dockerpng.png"
---

Hi friends, welcome back to Blogs-with-Achu, we have started the Docker Learning series, In my previous Blog we have seen about Container, Today in this blog we are Going to see Docker, Yes you heard that right?😉 According to Stack Overflow Survey-2020, Docker is the #1 most wanted platform,#2 most loved platform, and #3 most popular platform.

**In Today's Blog:**

- Introduction to Docker🙂

- Difference between Container and Docker💫

- Docker Architecture🏗️

- what next?⏭️

- Conclusion🏁

**Introduction to Docker**🙂

Docker is an open-source platform that enables developers to automate the deployment and management of applications within lightweight, isolated environments called containers. It provides a consistent and efficient way to package, distribute, and run software applications, regardless of the underlying infrastructure.

![](/my-demo-portfolio/static/blogs/docker-2.jpg)

**Difference between Container and Docker**💫

<table><tbody><tr><td>1) Docker is a popular platform that allows you to create and manage containers.<br><br><br><br><br>2) Docker provides the tools and infrastructure to build and run containers, making it easier to package, distribute, and deploy applications consistently across different environments.<br></td><td>1) Containers, on the other hand, are lightweight, isolated environments that package applications and their dependencies.<br><br>2) Containers are the encapsulated units that hold applications and make them portable and isolated</td></tr><tr><td></td><td></td></tr></tbody></table>

Docker vs Container

**_In simple terms✌️, Docker is like a shipping company that provides the platform and tools to package and deliver applications. Containers are like shipping containers used to transport goods. Docker uses containers to encapsulate applications, making them portable, isolated, and easily deployable across different environments._**

**Docker Architecture**🏗️

Before Learning Docker, Learning its Architecture is very important.

In simple terms, **Docker architecture consists of three main components**: **_the Docker client, the Docker host, and Docker images._**

1. **Docker Client**: The Docker client is the command-line interface (CLI) or graphical interface used to interact with Docker. It allows you to issue commands to Docker and manage containers, images, networks, and volumes.

3. **Docker Host**: The Docker host is the machine where Docker is installed and runs. It can be a physical or virtual machine (e.g., a server or a developer's computer). The host runs the **Docker daemon,** which is responsible for managing containers and handling Docker API requests from the client.

5. **Docker Images**: Docker images are the building blocks of containers. An image is a lightweight, standalone, and executable package that includes everything needed to run an application, such as the code, runtime environment, libraries, and dependencies. Images are created from Dockerfiles, which define the steps to build the image. Images can be stored and shared in registries like Docker Hub.

When you want to run an application using Docker, the Docker client communicates with the Docker daemon on the host. It sends commands to the daemon to perform actions like creating containers, pulling images, starting or stopping containers, and managing networks and volumes.

The Docker daemon then interacts with the host's operating system and manages the creation, execution, and lifecycle of containers based on the instructions in the Docker images. Each container runs in isolation, with its own filesystem, processes, and network interfaces.

**what next?**⏭️

In our upcoming blogs, we will learn how to install Docker on our local machine to prepare for hands-on experience. In the next blog, we will delve into Docker concepts such as Docker images, Docker containers, Docker Compose, and Docker volumes. We understand that learning Docker requires time and effort, and it cannot be mastered in a single day. Therefore, we need patience and a genuine interest to grasp the concepts effectively.

**Conclusion**🏁

If you have any doubts, please mention them in the comment section. I believe we have understood the concepts of containers and Docker. Let's keep up the enthusiasm and explore the real power of Docker in our upcoming blog. See you in the next blog. Happy learning and happy reading! 📖

Regards

Achanandhi M👦
