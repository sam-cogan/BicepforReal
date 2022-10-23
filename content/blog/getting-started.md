+++
title = "Getting Started"
date = 2022-10-22T16:32:38+01:00
weight = 1
draft = false
toc = false
author = "Sam Cogan"
+++

Welcome to the Bicep for Real course! This course aims to help you learn the Bicep Infrastructure as Code language, but also how this applies to the real world and how to use this language on real-world projects. 

If you just want to dive into the course straight away, head over to [Episode 1](../docs/Episode%201.md).

## Pre-requisites

This is a beginner's course and does not require previous experience with Bicep or Infrastructure as code. However, if you have never seen Bicep before, it might be worthwhile viewing the following videos from my "ARM (and Bicep) Masterclass" series which provides a quick introduction to the language and the concept of Bicep. There's no need to watch the whole series (unless you really want to understand how Bicep works under the hood).

- Introduction to Bicep: https://youtu.be/R636r-xcCMo

In terms of software needed to follow this course, we introduce most of this in [Episode 1](../docs/Episode%201.md), but you will need:

- A text editor of some sort, we use Visual Studio Code in the examples, and in my view, it is the best editor for working with Bicep
- A Git repository - this can be from any provider or just a local repository. In the course, we use GitHub, where you can create repositories for Free
- If you want to follow along with the automated pipelines section, you will want a pipeline tool. We use Azure DevOps pipelines in the examples, which are free and easy to use, but you can use your tool of choice, such as GitHub Actions, Jenkins, Circle CI, etc.

## Working Through the Course

This course is designed to take you through step by step and build on the previous week's work, so it is recommended you watch the classes in episode order. If you want to follow along and build the example infrastructure, you can complete the code for each episode, and you should have a deployable set of resources after each episode.

The source code I create for each episode is available in Git in [this repository](https://github.com/sam-cogan/lambda-toys-api-infrastructure). **Spoiler Alert** the main branch contains the source code as it as at the end of the course. If you want to view the source as it was at the end of a specific episode, you can look at the branches, and you will see a branch for most episodes. Each episodes branch is also listed on the [episodes page](/docs)


## The Scenario

The "for Real" part of this course is that we are building our infrastructure to satisfy a real-world type scenario that we will follow along for this project. [Episode 1](../docs/Episode%201.md) covers the scenario in detail, but if you want to read about the scenario or get the details for later review, you can see this below.

 We are creating infrastructure for a company called Lambda Toys. Their developers are hard at work creating a new container-based application that is going to replace their paper-based store ordering system with a brand-new digital store. We have been tasked with creating a process to deploy the infrastructure needed to support this project and meet its requirements.

![Lambda Toys](/images/lambda.png)

Lambda Toys have provided us with a set of requirements we need to meet when we create this infrastructure.

- Azure Only
- Run a multi-container based application
- Using DAPR
- NoSQL Database
- Access to data stores to be locked down
- API Security is critical
- Three Environments – Dev, Test & Prod
- Highly available within a region in production
- Active/Active across two regions in production
- Logging and Monitoring
- CI/CD for Infrastructure deployment
- Cost should be kept to a minimum


We have also created a high-level infrastructure diagram based on what we think will need to be deployed to meet these requirements.

![infrastructure diagram](/images/network.png)