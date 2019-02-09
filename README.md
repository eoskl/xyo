# AWS docker swarm based xyo nodes 
*aka: [wintersulgen](https://www.cafe-landei.de/) is coming*

* docker-stack.yml

As a first step I translated the instruction from [xyo](https://github.com/XYOracleNetwork/app-archivist-nodejs) into a docker swarm compose yml file. 

To create a Docker Swarm with variable amount of manager/worker nodes there is already excellent documentation [here](https://stelligent.com/2017/02/21/docker-swarm-mode-on-aws/)
Only caveat since we will be using external cloudstor volumes is to make sure the answer to Create EFS prerequisites for Cloudstor (Default is No) is selected 'YES'

Once the swarm is up you can ssh into one of the manager nodes and grep the yml file from the github repo.
* curl -O https://raw.githubusercontent.com/eoskl/xyo/master/docker-stack.yml

Then simply adjust the parameters as needed and bring up the stack with
* stack deploy -c docker-stack.yml xyo

mysql replication in swarm node taken from [here](http://ayoubensalem.me/tutorials/2018-04-03/Mysql-replication-in-Swarm-Mode)


To-Do list

- create volumes for the persistent data (Cloudstor)
- sizing aka: wintersulgen is coming!
