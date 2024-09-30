---
title: Google Cloud Beginner 
layout: home
parent: Devops 
---

# Creating Google Cloud Backend Server


## 1. Creating and Connecting to a Virtual Server Machine

1. Created account with Google Account

![google_cloud1](../../images/googlecloud1.png)


2. Create a new project and go to the console.

3. Start the beginner's guide on creating a web server.

![google_cloud2](../../images/googlecloud2.png)

4. Go to VM Instance Page and click on "Create Instance"

![google_cloud3](../../images/googlecloud3.png)

5. Create a machine that matches the computing power you want. Allow HTTP and HTTPS traffic.

![google_cloud4](../../images/googlecloud4.png)

6. When the status is ready, click on the SSH button to connect to the machine.

![google_cloud5](../../images/googlecloud5.png)

7. The terminal for the virtual machine will open.

![google_cloud6](../../images/googlecloud6.png)

## 2. Set a Fixed IP Address
1. Go to the external IP Address in the vm instance menu

![google_cloud7](../../images/googlecloud7.png)

![google_cloud8](../../images/googlecloud8.png)

## 2-1. Acquire Domain
* Go to google cloud domains 
* Rent domain there.

![rent domain](../../images/googlecloud9.png)
![setA](../../images/googlecloud10.png)

* Add Standard - > resource type A + ip v4 to our instance

![setA2](../../images/googlecloud12.png)

![setA3](../../images/googlecloud13.png)

Now my VM and server is set.

![googlecloudend](../../images/googlecloudend.png)