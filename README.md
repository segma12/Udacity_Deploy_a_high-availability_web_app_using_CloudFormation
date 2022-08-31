
# Deploy a high-availability web app using CloudFormation




The following artical contains instructions on how to deploy a highly available web application using AWS CloudFormation.


## Infrastructure Diagram

![Infrastructure Diagram](https://github.com/segma12/Udacity_Deploy_a_high-availability_web_app_using_CloudFormation/blob/master/project%202%20diagram.png?raw=true)


## Infrastructure Deployment

- Network. Includes VPC, two pairs of public, private subnets, Internet Gateway, NAT Gateways and Routing Tables for public, private subnets with associations.
- Application services. includes Load Balancer, security, target groups, Ubuntu servers and corresponding autoscaling. 


## Creating Stack

Creating the infrastructure stack run the following commands in the same order:

```bash
./create.sh infra-network  network.yml network-params.json                           
```

```bash
./create.sh infra-server  server.yml server-params.json
```
    
## Updating Stack

Updating the infrastructure stack run the following commands in the same order:

```bash
./update.sh infra-network  network.yml network-params.json                           
```

```bash
./update.sh infra-server  server.yml server-params.json
```