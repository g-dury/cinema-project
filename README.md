# cinema-project devops test

## Goal

Set up a full DevOps CI/CD pipeline from an open-source project.
For this exercise, between the 3 projects available I chose the second one called <br> **Cinema microservices** <br>
Url of the repo: <https://github.com/mmorejon/microservices-docker-go-mongodb>

## Tasks

The DevOps tasks given were 5:

* a) Run the whole application locally or in the cloud
* b) Run the whole application from images or other build artefacts
* c) Setup a log management solution and/or log analysis
* d) Setup a monitoring dashboard
* e) Setup a DevOps tool to manage different environment

I completed a) to c) successfully and have done bits of d) and e) regarding the tools I chose.
 
## Tools
 
Concerning the tools I had the choice among a lot of different tools to build a DevOps pipeline, lots of them are free or have a free trial limited in time which allow me to use them for this test.
As I am always eager to learn more I made some daring choices by choosing sometimes tools I was not familiar with.

### Cloud based deployment platform

I chose **AWS** for this exercise as it is the platform I am the more familiar with and has a free tier of 750h of server time.
I will give you EC2 access (read-only) and will give you also the key to access the servers

On top of AWS I used **Docker Community Edition (CE) for AWS (Docker-AWS-toolkit)** to abstract the layer of EC2 machines and just deal with a Docker Swarm Layer. Very interesting as I was not familiar with it at all.

### Build Service

I used **Travis-CI** which is a SaaS platform to provide a build server. I also chose this as I was not familiar and wanted to try it. The first setup is super easy as it is integrating easily with github.

### Artefacts Repository

I used **Docker Hub** as it is easily integrated into the docker stack
 
### Logs-related services

My choice was to use **Logz.io** to take all the advantages of the ELK stack without the trouble of setting it up on my own AWS infrastructure.

### Monitoring

I used **Updown.io** to set up a basic ping monitoring on my services. I am more familiar with Nagios but it does take some time to set up and I felt it was less relevant here.

## Deliverables

I will detail in the following part what I did exactly and how I set up the CI/CD Pipeline that you will see.