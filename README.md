# Udagram
In this project, I deployed web servers for a highly available web app using CloudFormation. I wrote the code that creates and deploys the infrastructure and application for an Instagram-like app from the ground up. I beginned with deploying the networking components, followed by servers, security roles and software. The procedure is following best practices and scripting as much as possible.

# Project - Deploy a high-availability web app using Cloudformation

As your final project, I was assigned to deploy an application (Apache Web Server), pick up code (JavaScript and HTML) from S3 Storage and deploy it in the appropriate folder on the web server.
To do so, I need to interpret the instructions as well as create a matching CloudFormation script.

# Problem

A company is creating an Instagram clone called Udagram. Developers pushed the latest version of their code in a zip file located in a public S3 Bucket.
I have been tasked with deploying the application, along with the necessary supporting software into its matching infrastructure.
This needs to be done in an automated fashion so that the infrastructure can be discarded as soon as the testing team finishes their tests and gathers their results.

# Project Requirements

- Server specs -

Create a Launch Configuration for my application servers in order to deploy four servers, two located in each of your private subnets. The launch configuration will be used by an auto-scaling group.
I'll need two vCPUs and at least 4GB of RAM. The Operating System to be used is Ubuntu 18. So, I need to choose an Instance size and Machine Image (AMI) that best fits this spec. Be sure to allocate at least 10GB of disk space so that I don't run into issues. 

- Security Groups and Roles -

Since you will be downloading the application archive from an S3 Bucket, you'll need to create an IAM Role that allows your instances to use the S3 Service.

Udagram communicates on the default HTTP Port: 80, so your servers will need this inbound port open since you will use it with the Load Balancer and the Load Balancer Health Check. As for outbound, the servers will need unrestricted internet access to be able to download and update its software.

The load balancer should allow all public traffic (0.0.0.0/0) on port 80 inbound, which is the default HTTP port. Outbound, it will only be using port 80 to reach the internal servers.

The application needs to be deployed into private subnets with a Load Balancer located in a public subnet.

One of the output exports of the CloudFormation script should be the public URL of the LoadBalancer.

Bonus points if you add http:// in front of the load balancer DNS Name in the output, for convenience.
