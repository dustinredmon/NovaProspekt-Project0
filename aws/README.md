##################################################################################################
# CIT480 - Group Project 0                                                                       #
# Team Name: NovaProspekt                                                                        #
# Team Members: Vlad Shtyrts, Dustin Redmon, Viktar Mizeryia                                     #
# Description: A basic one-page website hosted on Amazon Web Services                            #
# using VPC, EC2, Route53 DNS, HTML/CSS - https://novaprospekt.xyz/                              #
##################################################################################################
# 1. Features
#  - AWS Virtual Private Cloud (VPC) with public and private subnets
#  - AWS Elastic Compute Cloud (EC2) Instance running Ubuntu
#  - AWS Route53 to serve domain requests
#  - AWS Certificate Manager (ACM) for TLS/SSL Certifactes
#  
# 2. Installation
#  - Create AWS account and apply for student $100 credit
#  - Create VPC in the VPC dashboard with subnet 172.31.0.0/16
#  - Create Internet Gateway and attach to VPC
#  - Dvide subents into 3 public and private subnets
#       public 1    172.31.0.0/22   1024 IPs  us-west-2a  
#       public 2    172.31.4.0/22   1024 IPs  us-west-2b  
#       public 3    172.31.8.0/22   1024 IPs  us-west-2c  
#       private 1   172.31.16.0/20  4096 IPs  us-west-2a  
#       private 2   172.31.32.0/20  4096 IPs  us-west-2b
#       private 3   172.31.48.0/20  4096 IPs  us-west-2c
#  - Create Route Tables for public and private subnets and associate thier respective subnets.
#  - Add a route from any IP (0.0.0.0/0) to the Internet Gateway for the Public Route Table.
#  - Create EC2 instance in the EC2 dashboard using an Ubuntu 18.04 image on a public subnet.
#  - Create Hosted Zone in Route53 console with domain name novaprospekt.xyz
#  - Record NS records and input them with our domain provider NameCheap
#  - Create the following record sets for the Hosted Zone:
#       www.novaprospekt.com      A       "EC2 IP" or "TLS certificate"
#       novaprospekt.com          A       www.novaprospekt.com
#       google.novaprospekt.com   CNAME   www.google.com
#  - Request a certificate in the Certificate Manager dashboard using DNS validation.
#  - Edit the A record for "www.novaprospekt.com" and select the "TLS certificate" as the tartget value.
#  - Install Apache on the EC2 instance and test the configuration.
#
# 3. Contribute and Contact
#  - Dustin Redmon: dustin.redmon.39@my.csun.edu
#
# 4. LICENSE
#  - GNU GENERAL PUBLIC LICENSE
#
