---
title: "Getting Started With LocalStack"
dateString: August 2023
description: "LocalStack is a tool that runs on your local machine that emulates AWS API."
draft: false
tags: ["tech","AWS","cloudnative","LocalStack","Devops"]
weight: 106
authors: ["Achanandhi"]
cover:
    image: "/blogs/localstack-05.jpeg"
---


Hi friends🙋‍♂️ welcome back to Blogs-with-Achu, we have already seen the Introduction to LocalStack in our previous blog. **_LocalStack is a tool that runs on your local machine that emulates AWS API._** Now in this today's blog, we are going to explore and learn about LocalStack. The below image shows the working of LocalStack.

![](https://achanandhi.wordpress.com/wp-content/uploads/2023/08/whatsapp-image-2023-08-20-at-9.48.19-pm.jpeg?w=1024)

Image credit: KodeKloud

**Today's Agenda**:

1. **How to install LocalStack on your local machine🤔?**

3. **AWS Services on LocalStack**

5. **How to integrate LocalStack?**

7. **Summary**

1\. **How to install LocalStack on your local machine🤔?**

The first thing I want to mention here is that there is no management console, likewise, we see in AWS Management Console, In LocalStack everything we will be working with the command line.

My best choice for learning or for the installation of any service, I will prefer documentation. [Documentation](https://docs.localstack.cloud/getting-started/installation/) is the best part of getting started.

The below image shows the LocalStack Installation Docs

![](/my-demo-portfolio/static/blogs/localstack-07.png)

**_Use documentation for installation purposes._** There are multiple ways you can install LocalStack, it depends on your use case. you can install a LocalStack based on your platforms, apart from there are different ways you can install LocalStack, you can install by using LocalStack CLI, docker,docker-compose, and also using helm. Choose the one that best suit for your use case. **_Remember LocalStack runs on a docker container._** I installed LocalStack using docker.

2\. **AWS Services on LocalStack**

LocalStack provides emulation services for different AWS APIs. Almost every service is available in LocalStack, you can use Services like S3, Lambda, IAM, ECR, EC2, EKS, etc. But the issue is here is you can't use EKS for Community Edition, and for that, you need to pro user. Don't there are other Services you can use for testing purposes? Here is the list of services LocalStack offers.

![](/my-demo-portfolio/static/blogs/localstack-08.png)

**3\. How to integrate LocalStack?**

Now it's time for making our hands dirty, get ready with your command line. verify LocalStack is installed on your machine

```
localstack --version 
```

```
localstack start 
```

![](/my-demo-portfolio/static/blogs/localstack-09.png)

LocalStack start will start the LocalStack docker container. If you got similar output like this, you are on the correct path, if not you need to evaluate and try to fix the issue. If are unable to fix it please post in the comment section. It is better to use to sudo in front of the LocalStack command.

**Integrations**

Next, open the new tab in the terminal, don't use the same tab where you ran the initial start command. Next, steps are the most important step in working with LocalStack, you need to integrate LocalStack to use cloud resources. Switch to the [Integrations](https://docs.localstack.cloud/user-guide/integrations/) page:


![](/my-demo-portfolio/static/blogs/localstack-10.png)

There are multiple ways you can integrate based on your needs, we are now focusing mainly on the AWS Command line interface, it is a very important integration, it will only send the incoming endpoint to LocalStack instead of sending it to AWS. Don't forget to integrate, otherwise, you will not get the desired output.

Click [the AWS Command line](https://docs.localstack.cloud/user-guide/integrations/aws-cli/) interface in the left-side menu

![](/my-demo-portfolio/static/blogs/localstack-11.png)

In the overview section, there are two CLI alternatives, they both will give the same result.

(i) **AWS CLI Setup**

![](/my-demo-portfolio/static/blogs/localstack-12.png)

If you want to use AWS CLI you can follow this one, and also forget to read the Note. Use the "test" as a value for aws\_access\_key and for aws\_secret\_key. Don't forget to change or include the endpoint URL, the endpoint URL is used to divert the request to the LocalStack endpoint instead of sending it to AWS.

**(ii) LocalStack AWS CLI**

![](/my-demo-portfolio/static/blogs/localstack-13.png)

LocalStack AWS CLI is created by Localstack, for interacting with locally created services through API. I prefer to use to LocalStack AWS CLI it best way to get started. You can what best suits you, both are the same

**4**. **Summary**

In this blog, we installed LocalStack locally on our machine and we configured the endpoint URL to divert the request to LocalStack ie (integrations). Don't forget to integrate it is a very important process. We have already seen enough theory, In our upcoming LocalStack blog we see, how actually we work with AWS services locally using LocalStack. In the next blog, we see how to work with S3 locally. See you in Next Blog. If you find it useful please share it with your friends and let others also make use of it. Happy learning and happy reading! 📖

Regards

Achanandhi M👦
