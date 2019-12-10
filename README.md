# ec2_instance_ansible
Terraform template to create an ec2 instance and bootstrap to Ansible

## Prerequisites
- Access to Scalr Next Gen
- An Ansible Server
- An Ubuntu AMI. This exmaple assumes Ubuntu is used.

IMPORTANT: This is meant to be used with the Scalr Next Gen Service Catalog.

The following policies must exist for AWS in Scalr:

cloud.locations
cloud.subnets
cloud.instance.types
cloud.security_groups

The following Global Variables must exist in Scalr:

`key` - The key that will be used for the server provisioned in AWS

`ami` - The ami to be used in the Terraform template.

The tutorial for this template can be found here: https://scalr-athena.readthedocs-hosted.com/en/latest/next-gen/service_catalog.html#example

## Ansible

This will bootstrap to an Ansible server. This assumes that you already have an Ansible server created. The following variables will be used for the Ansible integration:

`remote_host` - The Ansible server IP or DNS name.

`ssh_private_key` -  The key used to connect to the Ansible server through remote-exec.
