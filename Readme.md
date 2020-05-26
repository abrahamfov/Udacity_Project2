# Udacity's Cloud Devops Engineer Nanodegree
## Project #2: Deploy a High-Availability Web App using CloudFormation

# Overview
This is a Cloud Formation setup to deploy an infrastructure and its resources for a highly available app as requirement to Cloud DevOps Nanodegre of Udacity.

## To create a stack:

./create.sh stackname template-body parameters

Example for infrastructure:
./create.sh udagram /Templates/network.yml /Parameters/network-parameters.json

Example for servers:
./create.sh udagram /Templates/servers.yml /Parameters/servers-parameters.json

## To update a stack:

./update.sh stackname template-body parameters

Example for infrastructure:
./update.sh udagram /Templates/network.yml /Parameters/network-parameters.json

Example for servers:
./update.sh udagram /Templates/servers.yml /Parameters/servers-parameters.json

## To delete a stack:

./delete.sh stackname

# Infrastructure Diagram
![Alt text](/Udagram_Project_Abraham.png)
