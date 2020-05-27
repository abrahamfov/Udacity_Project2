# Udacity's Cloud Devops Engineer Nanodegree
## Project #2: Deploy a High-Availability Web App using CloudFormation

# Overview
This is a Cloud Formation setup to deploy an infrastructure and its resources for a highly available app as requirement to Cloud DevOps Nanodegre of Udacity.

LoadBalancer URL: 	http://udagr-WebAp-1P1XM5QW87ZGU-231856614.us-west-2.elb.amazonaws.com
(This link is available at the moment of submission of the project)

## To create a stack:

./create.sh stackname template-body parameters

Example for infrastructure:
./create.sh udagram ./Templates/network.yml ./Parameters/network-parameters.json

Example for servers:
./create.sh udagram ./Templates/servers.yml ./Parameters/servers-parameters.json

## To update a stack:

./update.sh stackname template-body parameters

Example for infrastructure:
./update.sh udagram ./Templates/network.yml ./Parameters/network-parameters.json

Example for servers:
./update.sh udagram ./Templates/servers.yml ./Parameters/servers-parameters.json

## To delete a stack:

./delete.sh stackname

## Settings for bastion hosts

Within the servers configuration file, there are some lines referring to bastion hosts connections through port 22, allowing the SSH connection if needed for maintenance purposes. This feature is shown in the architecture diagram, but as it needs to allocate the .pem files, it would be mandatory to generate them for connecting to local IP and to save SSH to private servers in bastion hosts. It is mandatory to respect the syntaxis of the bastion hosts in order to have some names generated as outputs to allow the servers scripts to update the connection permissions of the EC2 instances.

## IAM Role and IAM Instance Profile

Both of these features are deployed within the infrastructure stack, and are available from the AWS CloudFormation outputs, in order to be used in the launch configuration settings.

# Infrastructure Diagram
![Alt text](/Diagram/Udagram_Project_Abraham.png)
