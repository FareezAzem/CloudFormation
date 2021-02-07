# CloudFormation

This is a cloudformation script to deploy network infrastructure and servers for a highly available webapp.


## Important files
- Network.yml deploys a VPC, with public and private subnets spread across two Availabilty Zones. It deploys an Internet Gateway, with a default route on the public subnets. It deploys NAT Gateways (one in each AZ), and default routes for them in the private subnets.
- NetworkParams.json is the parameters needed to deploy that network infrastructure script.

- Servers.yml deploys LoadBalancer, Launch Configuration, AutoScaling group a health check, security groups and a Listener and Target Group.
- serverParams.json is the parameters needed to deploy that servers for the webapp.
