---
title: "Exploring 🐬the World of Containers"
dateString: July 2023
description: ""
draft: false
tags: ["Contanier","Devops","Docker","DockerHub","tech", "VM"]
weight: 114
authors: ["Achanandhi"]
cover:
    image: "/blogs/container.jpg"
---

_**Use Container for deployment**_

Hi friends, welcome back to Blogs-with-Achu! In today's fast-paced technological landscape, containers have emerged as a powerful software development and deployment solution. If you're interested in learning containerization, you don't need any specific prerequisites.😁

**In Today's Blog:**

- What is Container?🤔

- Why it is so popular?🤔

- Is VM?☠️

- Containerization Technology💻

- Summary🏁

**What is Container?**🤔

A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another.

This may sound complicated let's see with an example, Imagine you and your friend are both software developers working on a project. You develop the code on your Linux operating system using a specific version of a database, let's say MySQL 5. However, your friend works on a Windows machine and uses the latest version of MySQL.

During development, everything works smoothly on your respective machines. The code and functionality are perfect. However, when it comes time to deploy the application to a production environment, problems arise. The application encounters compatibility issues when it's deployed on a different server or operating system. The database version on the production server might not be the same as what you used during development, causing conflicts and errors.

Here's where containerization comes to the rescue. Think of containerization as a special box that contains not only your code but also all the necessary components for it to run correctly, including the specific database version. By using containers, you can package your application, along with the required database version and any other dependencies, into a self-contained unit. This is not only applicable to databases, any application can be containerized.

**Why it is so popular?**🐬

I think you might be guessed why it is so popular. Let's see them 😉

Containers have become popular due to their **_portability, scalability, efficiency, alignment with DevOps practices, compatibility with cloud-native technologies, and the robust ecosystem of tools and technologies that support containerization_**. Containers empower developers and operations teams to build, deploy, and manage applications more effectively, ultimately improving productivity, agility, and scalability in software development and deployment processes.

**Is VM dead?**☠️

_**I think why might be wondering which one is replaced by a container, it is nothing but a Virtual machine**_. VM is not actually dead, but it's lost its popularity among developers.

**Let's difference between VM and container**

![](/my-demo-portfolio/static/blogs/vm-vs-docker.png)

- Containers virtualize the operating system and provide an isolated runtime environment for applications within the host OS.

- VMs virtualize the entire infrastructure, including hardware, and enable the execution of multiple independent operating system instances on a single physical machine.

- Special software Hypervisor is useful for virtualizing the underlying infrastructure in virtual machines (VMs), providing hardware-level virtualization, and managing the allocation of physical resources to multiple VMs.

- Docker Engine is useful for containerization, providing a runtime environment and tools for building, running, and managing containers.

**Containerization Technology**

Docker and Kubernetes are popular containerization technologies that have transformed application development, deployment, and management.

![](/my-demo-portfolio/static/blogs/ultimate-containerization.webp)

**_Docker simplifies containerization by providing tools to create and run lightweight, isolated containers. Kubernetes focuses on container orchestration, automating deployment, scaling, and management._**

**Conclusion** 🏁

Don't worry if you are not familiar with Docker and Kubernetes, this blog is just an introduction. We will see upcoming concepts in our later blogs. Hereafter, my focus is mainly on containerization and its technology. If you want to learn containerization with me, you are always welcome. Please subscribe to get regular updates regarding containerization. See you in the next blog. Happy learning 📖

Regards

Achanandhi M👦
