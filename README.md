# AWS docker swarm based xyo nodes (aka: wintersulgen is coming)

* docker-compose.yml
As a first step I translated the instruction from https://github.com/XYOracleNetwork/app-archivist-nodejs into a docker swarm compose yml file. 

To create a Docker Swarm with variable amount of manager/worker nodes there is already excellent documentation here

https://stelligent.com/2017/02/21/docker-swarm-mode-on-aws/

since we will be using external cloudstor volumes please make sure the below answer is 'YES'

Create EFS prerequsities for CloudStor?
Create CloudStor EFS mount targets

To-Do list

- create volumes for the persistent data (Cloudstor)
- sizing?
