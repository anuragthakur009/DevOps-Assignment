# DevOps-Assignment
Overview
This repository contains AWS CloudFormation templates for provisioning a network architecture, VPN client, and an Aurora Serverless RDS database. The templates are designed to fulfill the specified requirements for a shared system network and a development system network.

Repository Structure

•vpc-template.yaml: CloudFormation template for creating a VPC with public and private subnets.

•vpn-template.yaml: CloudFormation template for deploying an AWS VPN client.

•rds-template.yaml: CloudFormation template for provisioning an Aurora Serverless RDS database.

•peering-template.yaml: CloudFormation template for establishing VPC peering between the shared system network and the development system network.

USAGE
1.Deploying VPCs

Execute vpc-template.yaml twice, once for each VPC (shared-system-network and dev-system-network).
Provide necessary parameters such as VpcCidrBlock, PublicSubnet1CidrBlock, etc.

2.VPC Peering

Execute peering-template.yaml to establish VPC peering between the two VPCs.
Provide parameters like VpcId1 and VpcId2.

3.Deploying VPN Client

Use vpn-template.yaml to deploy the AWS VPN client on the  shared system network VPC.
Ensure proper configuration with the VPC and VPN parameters.

4.Deploying RDS Database

Execute rds-template.yaml to create an Aurora Serverless RDS database in the private subnets of the development system network VPC.
Provide parameters including DBInstanceIdentifier and VpcId.

INSTRUCTIONS

1.Customization

Customize parameter values in each template according to your specific requirements.

2.Deployment Order

Deploy VPC templates (vpc-template.yaml) first.
Establish VPC peering using peering-template.yaml.
Deploy VPN client (vpn-template.yaml) on the shared system network.

Finally, deploy RDS database (rds-template.yaml) on the development system network.

3.GitHub Repository

Visit https://github.com/Vanisher47/DevOps-Assignment/tree/main  for the source code.
Author
Name: Ambuj Parag Mishra
GitHub ID: Vanisher47
