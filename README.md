# terraform-course.
* Terraform Version : v0.12.24

* Orignal Source form : [https://github.com/wardviaene/terraform-course](https://github.com/wardviaene/terraform-course) for  [Udemy course about Terraform](https://www.udemy.com/learn-devops-infrastructure-automation-with-terraform/?couponCode=TERRAFORM_GIT)
* Update by Steve J.South [NamJungGu] <nowage@gmail.com>

# Usage
```
cd
git clone https://github.com/Finfra/terraform-coursehttps://github.com/Finfra/terraform-course
cd terraform-course/01-FirstSteps
cat README.md
```

# Demo overview
Demo Directory                                  | Description
------------------------------------------------| -------------
01-FirstSteps                                   | First steps : One File Version
02-FirstSteps_files                             | First steps : File Separate
03-Provisioner_basic                            | Enable Login : One File Version
04-Provisioner_files                            | Enable Login : File Separate
05-Provisioner_Script                           | Using provisioner : Script
06-ExecutingScriptLocally                       | Executing script locally
07-Outputting                                   | Outputting : S3
08-DataSource                                   | Data Source : Security Groups Create
09-Modules                                      | Modules : Consul Module from github
10-AwsVpc                                       | AWS VPC
11-Ec2VpcSecuritygroup                          | EC2 instance within VPC with securitygroup
12-Ec2EBS                                       | EC2 instance with EBS volumes
13-UserdataAndCloudinit                         | Userdata and cloudinit
14-Route53                                      | Route53 (DNS)
15-RDS                                          | RDS
16-IAM                                          | IAM
17-IAMRolesWithS3Bucket                         | IAM Roles with S3 bucket
18-Autoscaling                                  | Autoscaling
19-AutoscalingWithELB                           | Autoscaling with ELB (Elastic Load Balancer)
20-ElasticBeanstalk                             | Elastic Beanstalk PHP 7 stack with RDS
21-InterpolationsVPCModule                      | Interpolations, VPC module
22-ProjectStructure                             | Project structure, best practices
23-packer                                       | Build AMIs with Packer
24-jenkins-packer                               | Demo with jenkins and Packer
c0-MultiInstance                                | Demo for MultiInstance
c1-EKS                                          | Demo with EKS
c2-UsingProvisionerOnWindowsInstance            | Using provisioner on a Windows instance
c3-docker_local                                 | Using Local Docker
c4-docker_EcrContainerRegistry                  | Using ECR - The EC2 Container Registry
c5-docker_EcsContainerService                   | Using ECS - The EC2 Container Service
c6-docker_EcrEcsWithJenkinsInACompleteWorkflow  | Using ECR/ECS with Jenkins in a complete workflow
c7-module2                                      | Using ECS + ALB in 4 modules to show how developing terraform modules work

# Setting for Convenient
* Root계정에서 실행하세요.
```
## ssh
echo "    StrictHostKeyChecking no" >> /etc/ssh/ssh_config

## EDITOR
echo "export EDITOR=vi" >> /etc/bash.bashrc

## Alias for Terraform Apply
cmd='
terraform destroy -auto-approve
terraform init
terraform apply -auto-approve
cat terraform.tfstate|grep public_ip|grep -v associate
'
echo "alias ta=\"echo '$cmd';$cmd\"">>/etc/bash.bashrc

## Alias for Terraform Destroy
cmd='terraform destroy -auto-approve
'
echo "alias td=\"echo '$cmd';$cmd\"">>/etc/bash.bashrc

## Alias for Delete aws Key pair
cmd='aws ec2 delete-key-pair --key-name mykey
'
echo "alias dk=\"echo '$cmd';$cmd\"">>/etc/bash.bashrc
```
