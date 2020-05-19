---
title: Introduction to Cloud9 IDE
summary: Configure and use Cloud9 IDE
tags:
- Cloud 9
date: "2020-05-17T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  focal_point: Smart

# links:
# - icon: twitter
#   icon_pack: fab
#   name: Follow
#   url: https://twitter.com/georgecushen
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: cloud9
---

# Containers University

{{< vimeo 419093608 >}}

## Introduction to AWS Cloud9 - 900 level

- Welcome to the Introduction to AWS Cloud9! The goal of this chapter is to gain a better understanding of how we can setup a cloud based IDE in AWS, and use it's features to speed up development cycles.
- We will look at what Cloud9 provides us as an IDE for AWS, and look at the features and configurations available. Lastly, we will learn how we can use Cloud9 to manage resources in AWS.

# Video 1

{{< vimeo 419093636 >}}

### Introduction
- In this section, we're going to talk quickly about why we may want to use an IDE, and then we're going to look at how to get started.

### What is an IDE and why use one

- An IDE (interactive development environment), consolidates programming tasks into one place. An IDE has features to enable developers to get their work done faster. With Cloud9 being in the cloud means you can work on your projects from your office, home, or anywhere using an internet-connected machine.
- Some features that a developer will get from an IDE are:
  - Code completion
  - Syntax highlighting
  - build/debugging tools
  - testing/linting frameworks

### Getting started/Pre-requisites
- To get started with Cloud9, you will need the following:
  - An AWS Account
  - Appropriate permissions via IAM create, and use the Cloud9 instance.
- Next, you will want to look at your usage pattern to determine how to proceed. In the example today, we will be setting up Cloud9 as the only individual using the AWS account.
  - Please note the other patterns, such as multiple users same account, or an enterprise with using SSO.

In the next section we'll walk through creating a cloud9 instance, as well as briefly review the environment.

# Video 2

{{< vimeo 419093741 >}}

### Introduction
- In this section, we will build a Cloud9 instance, and briefly review the interface.

### Creating a Cloud9 Instance

##### Via console
- To create a Cloud9 instance via the console, we will first navigate to the Cloud9 service page:
    - https://us-west-2.console.aws.amazon.com/cloud9/home/product
- Next, click `Create Environment`
- Now that you are in the environment creation screen, let's look at some of the different options available:
  - Environment type:
    - There are two ways to create environments. In the example here, we will be creating an `EC2 environment`. See here for more details on other ways to create environments: https://docs.aws.amazon.com/cloud9/latest/user-guide/create-environment.html
    - SSH environment allows cloud9 to access a server via ssh to setup Cloud9 on a remote server.
  - Instance type:
    - This is where you can select the size of instance you want Cloud9 to use. Depending on your use case, choose the instance size that is appropriate. For the demo, we will choose t2.micro.
  - Platform:
    - Amazon Linux or Ubuntu Server - You can choose based on preference of underlying OS. For the demo, we will stick with Amazon Linux.
  - Cost saving setting:
    - You can choose a predetermined amount of time to auto-hibernate when the IDE is not in use. This is to save money and not pay for resources that are not being used.
  - IAM role:
    - Cloud9 will create a role that will allow cloud9 to access other resources on your behalf.
  - Network settings:
    - VPC/Subnets can be chosen here.
- Once you select the settings, click `Next`.
- Review the configuration, and when ready click `Create environment`. This will begin building the IDE. 
  - You should see the IDE open in the browser. It will take a couple of minutes for the IDE to be ready to go. 
    
#### Via automation (CloudFormation)
- See [here](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloud9-environmentec2.htm)

### Accessing the Cloud9 IDE

{{< vimeo 419104079 >}}

### Introduction

- In this section, we will learn how to access our Cloud9 environment, as well as test the IDE with a couple simple lines of python code.

##### AWS Console
- To access Cloud9, search for Cloud9 under services.
- In the console, you can see your environments. If someone created an environment that is shared with you, you can see that under `Shared with you` on the left hand side.
- Find your IDE, and click `Open IDE`. This will open Cloud9 in the browser.

### Cloud9 experience

- Let's look around Cloud9. When we first log in, we see a terminal at the bottom, and a welcome page at the top. We can format this to fit our personal preferences.
- Close the top tab, and let's create some code.
- In the terminal, create a file called testing.py
```bash
touch testing.py
```
- Let's list the directory, find the file, and open it. This can be done in a few ways, but for this example, let's click the file and select `Open`
- Now, let's add some code and see how we can run it in the IDE. I recommend typing these commands into the IDE to get a feel for the features that are available, such as autocompletion.
```python3
#!/usr/bin/env python3

import os

directory_contents = os.listdir()

print(directory_contents)
```
- In the top, click `Run`
  - We should now see a python terminal open and watch the code run successfully.
- Next, let's introduce broken code and see how the IDE reacts.
```python3
directory_contents = os.listdir(undefined_variable)
```
- Before we click run, notice that there is a red x next to the line where we added the new code. Hover over it, and you'll see that it is telling us that we have introduced an undefined variable. But, let's not trust it and go ahead and run the code.
- Click `Run`, and you should see in the terminal an error. Had we listened to the IDE, we could have avoided this tragedy!
- That's it for a basic high level experience with the IDE.

##### Settings

##### Language support

##### Configuration

### Recap

