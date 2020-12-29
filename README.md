# Udagram
In this project, I deployed web servers for a highly available web app using CloudFormation. I wrote the code that creates and deploys the infrastructure and application for an Instagram-like app from the ground up. I beginned with deploying the networking components, followed by servers, security roles and software. The procedure is following best practices and scripting as much as possible.

# Project Introduction - Deploy a high-availability web app using Cloudformation

As your final project, I was assigned to deploy an application (Apache Web Server), pick up code (JavaScript and HTML) from S3 Storage and deploy it in the appropriate folder on the web server.
To do so, I need to interpret the instructions as well as create a matching CloudFormation script.

# Problem:

A company is creating an Instagram clone called Udagram. Developers pushed the latest version of their code in a zip file located in a public S3 Bucket.
I have been tasked with deploying the application, along with the necessary supporting software into its matching infrastructure.
This needs to be done in an automated fashion so that the infrastructure can be discarded as soon as the testing team finishes their tests and gathers their results.
