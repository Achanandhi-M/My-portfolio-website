---
title: "Docker🐬 Dreams💭-1"
description: "Docker for Begineer Series"
dateString: July 2023
draft: false
tags: ["Contanier","Devops","Docker","DockerHub","tech"]
weight: 111
cover:
    image: "/blogs/dockerpng.png"
---

Hi friends🙋‍♂️ welcome back to Blogs-with-Achu, we have started the Docker🐬 Learning series, In my previous Blog⏮️ we saw about _**how to install docker on our local system and we saw some basic docker commands.**_

**Today's blog agenda:**

1. Understanding Docker Images and Containers😎

3. Unleashing the Power of Docker💪

5. Discover Dockerhub: An Abundance of Useful Resources💫

7. Working with Docker Images and Containers: Real-Life Examples⚒️

9. What's Next in our Docker Journey?⏭️

11. Conclusion🏁

1) **Understanding Docker Images and Containers**😎

Before working with Docker🐬 it is crucial to understand the concepts of images and containers because they are essential in Docker. In my previous blog⏮️ we discussed containers, which are lightweight and run in an isolated environment. However, you may be wondering**_, What are images and why do we need them to create Docker containers?_** These questions have arisen as I learn about Docker.

Let's see the answer with the simple analogy of ordering🍽️ and cooking🍳 food, let's relate it to Docker🐬

1. **Image**: An image is like a menu in a restaurant🏨. It lists various dishes🍪 and provides details about the ingredients, cooking instructions, and presentation. Just like you choose a dish from the menu, in Docker, you select an image that represents a specific application or environment you want to run.

3. **Container**: A container is like a chef🧑‍🍳 who receives the order and cooks the food according to the selected dish from the menu. When you order a dish, the chef creates a separate cooking area and prepares the dish with the specified ingredients and cooking instructions. Similarly, when you create a container from an image, Docker sets up an isolated runtime environment where the application or processes defined in the image run🏃‍♂️.

**Here's how the process works with Docker:**

1. Imagine you're in a restaurant that offers a wide range of dishes (images) on its menu.

3. You browse the menu and select a specific dish (image) that you want to order. For example, you choose a **_"Web Server"_** dish from the menu, which represents an image with all the necessary components to run a web server.

5. You place your order with the waiter, who acts as **_Docker in this analogy_**. You tell Docker to create a container based on the "Web Server" image.

7. Docker takes the **_"Web Server" image (recipe)_** and sets up a separate cooking area, which is an isolated runtime environment (container).

9. Inside the container, Docker follows the instructions provided by the image and sets up the web server, installs the required software, and configures the necessary settings.

11. The container is now running, and your web server is ready to serve requests. Just like the chef cooking your food, the container is executing the processes defined in the image.

13. The container remains separate from other containers and the underlying host system, ensuring isolation and security.

15. If you need to run multiple instances of the web server, you can order multiple containers based on the same "Web Server" image, just like requesting multiple servings of the same dish .

**_In this analogy, Docker acts as the intermediary between you (the customer) and the chef (the container). It takes your order (image) and creates a separate cooking area (container) where the specified dish (application or processes) is prepared._**

In Docker, containers are created from images. You cannot create a container without an image. An image in Docker serves as a template or blueprint that contains all the necessary instructions, dependencies, and files required to create and run a container. The image defines the environment and the processes that will run inside the container.

**So, in summary, an image is a prerequisite for creating a container. The image provides the necessary instructions and dependencies, while the container is the actual running instance that is created based on the image.**

2\. **Unleashing the Power of Docker**

You can use Docker for anything, For example, you can find Docker images for popular databases like MySQL, PostgreSQL, and MongoDB. There are also images for web servers like Apache HTTP Server and Nginx, programming languages like Python, Java, and Node.js, development frameworks like Ruby on Rails and Django, and many more.

In addition to specific software components, Docker images can also include custom configurations, scripts, or additional dependencies needed for your application to run properly.

3\. **Discover Dockerhub: An Abundance of Useful Resources**💫

We already know that images are important for creating a Docker container, which is useful for establishing an isolated environment. But where on earth are those images present? They reside in Dockerhub, the official website of Docker, where millions of Docker images are available. You can pull and push your Docker images to Dockerhub so others can make use of them.

Use this link to visit the magical world of Docker [click here](https://hub.docker.com/)

![](/my-demo-portfolio/static/blogs/dockerhub-01.png)

The above image shows the home page of the Docker hub, in the top right-hand side it shows my name because I created an account in the docker hub, In the Docker hub u can also host our own docker images and also there is the option of creating private repositories.

![](/my-demo-portfolio/static/blogs/dockerhub-02.png)

The above picture shows the images present in the Dockerhub, u can search the image based on your requirements. U have the option to filter out based on your operating system and Architecture.

4\. **Working with Docker Images and Containers: Real-Life Examples**⚒️

After identifying the desired image for your application, you can easily use or pull that image from Docker Hub. Don't worry, there is a command specifically for this purpose:

```
docker pull <image name>
```

You can use this command to pull the Docker image from Dockerhub

**Lets's see with an example - Hello world🌏 in Docker**

Get ready for hand on open up your terminal and type these commands in your command line

```
docker run hello-world
```

The hello-world is a pre-build image in the Docker hub, which displays hello world in the terminal. Wait, earlier I said if you want to pull any image you can use the **docker pull command**, but now I have not used it the reason for that is if you use the docker run command, It will check the image locally, if the image is not present in locally, it will automatically pull the image from docker hub and it creates the container for running, it is the real power of using docker run command.

![](/my-demo-portfolio/static/blogs/docker-exec-2.png)

The above picture shows the output, if you got the same output as me, congratulations🎉 we've done it. Don't forget to use sudo before docker commands. I am using the(Ubuntu) Linux operating system, so I am using sudo the reason for that is using `sudo` with the `docker` commands is required when running Docker as a non-root user, as it allows the command to be executed with administrative privileges. Docker requires elevated permissions to access system resources and manage containers. Running Docker commands with `sudo` ensures the necessary privileges are granted, enabling successful execution of Docker operations.

![](/my-demo-portfolio/static/blogs/docker-ex1-1.png)

The output shows the container is not running. By default, a Docker container will stop once the main process running inside the container completes its execution. This means that when the process specified in the Docker image's entry point or command finishes running, the container will automatically stop.

```
docker run -d <image_name>
```

However, you can override this default behavior by specifying additional options or configurations when running the container, such as using the `-d` flag to run the container in detached mode and keep it running in the background.

**What's Next in our Docker Journey?**⏭️

Congratulations🎉 we successfully 💥deployed and run our first container, don't lose the spark, there is much more to explore in upcoming blogs. In our next blog, we will see the different types of flags used in docker commands and some examples, but trust me you really like the example.

**Conclusion**🏁

If you have any doubts, please mention them in the comment section. Let's keep up the enthusiasm and explore the real power of Docker in our upcoming blog. See you in the next blog. Happy learning and happy reading! 📖

Regards

Achanandhi M👦
