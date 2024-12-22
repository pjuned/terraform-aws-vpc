AWS VPC MODULE
****************

This module created following resources. We are getting HA.we are getting first 2 AZ's automatically

VPC
Internet gateway VPX Association
2 public subnets in 1a & 1b
2 private subnets in 1a & 1b
2 database subnets in 1a & 1b
Elastic IP
NAT gateway in 1a public subnet
public route table
private route table
database route table
Subnets & route table associations
VPC peering if user requests
Adding the peering route in default VPC, if user dont provide acceptor VPC explicitly.
Adding the peering route in public , privarte & database route tables

Inputs
*******

Project name (required) - your project name
environment (Required) - which environment you are working in
vpc_cidr (optional) - default is 10.0.0.0/16, user can override
enable_dns_hostnames(Optional) - Default value is true
common_tags(OPtional) - better to provide
vpc_tags(optional) 
igw_tags (optional)
public_subnets_cidr(Required) - user must provide 2 valid public subnets CIDR
public_subnets_tags (optional) - Default is empty, type is map
private_subnets_cidr(Required) - user must provide 2 valid private subnets CIDR
private_subnets_tags (optional) - Default is empty, type is map
database_subnets_cidr(Required) - user must provide 2 valid database subnets CIDR
database_subnets_tags (optional) - Default is empty, type is map
nat_gateway_tags(Optional) - Default is empty, type is map
public_route_table_tags (Optional) - Default is empty, type is map
private_route_table_tags (Optional) - Default is empty, type is map
database_route_table_tags (Optional) - Default is empty, type is map
is_peering_required(optional) - default value is default VPC id
acceptor_vpc_id (Optional) - default value is default vpc id
VPC -Peering -tags (Optional) - Default is empty, type is map

Outputs:
*********
vpc_id =  VPC ID created
public_subnet_ids - 2 public subnetids created
private -subnet_ids - 2 private subnet Ids created

