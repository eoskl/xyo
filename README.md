# AWS docker swarm based xyo nodes (aka: wintersulgen is coming)

* docker-stack.yml

As a first step I translated the instruction from [xyo](https://github.com/XYOracleNetwork/app-archivist-nodejs) into a docker swarm compose yml file. 

To create a Docker Swarm with variable amount of manager/worker nodes there is already excellent documentation [here](https://stelligent.com/2017/02/21/docker-swarm-mode-on-aws/)

Once the swarm is up you can ssh into one of the manager nodes and grep the yml file from the github repo.
* curl -O https://raw.githubusercontent.com/eoskl/xyo/master/docker-stack.yml

Then simply adjust the parameters as needed and bring up the stack with
* stack deploy -c docker-stack.yml xyo

since we will be using external cloudstor volumes please make sure the below answer is 'YES'

Create EFS prerequsities for CloudStor?
Create CloudStor EFS mount targets

To-Do list

- create volumes for the persistent data (Cloudstor)
- sizing?
