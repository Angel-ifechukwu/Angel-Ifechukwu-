# Deploying an infrastructure using Ansible script and Terraform 


## Introduction:
 
 This README document provides instructions on how to deploy an infrastructure using Ansible and Terraform. The deployment includes creating a new virtual machine, configuring it with Ansible, and installing necessary software.

## Requirements:

* A machine running Linux OS (Ubuntu, Debian, CentOS)
* Ansible version 2.10 or later installed on the machine
* Terraform version 0.12 or later installed on the machine
* Access to a cloud provider account (such as AWS, Azure, or Google Cloud)

## Deployment Process:

* Clone the repository containing the deployment scripts from the Git repository to your local machine.
* Navigate to the root directory of the cloned repository.
* Update the variables in the "variables.tf" file as per your requirements.
* Run terraform init command to initialize the Terraform configuration and download necessary plugins.
* Run terraform plan command to check the deployment plan.
* If the plan looks good, run terraform apply command to create the infrastructure.
* After the infrastructure is created, update the inventory file "hosts.yml" with the IP address of the newly created virtual machine.
* Run the Ansible playbook using the command `ansible-playbook -i hosts.yml playbook.yml`
* The playbook will configure the virtual machine as per the playbook instructions.

## Additional Notes:

* Before running any commands, make sure you have configured your cloud provider credentials on your machine.
* You may customize the Ansible playbook and Terraform configuration as per your requirements.
* Once the deployment is complete, verify that the virtual machine is running and all the necessary software is installed.
* To delete the infrastructure, run `terraform destroy` command from the same directory where you ran `terraform apply` command.
* In case of any errors or issues during the deployment process, refer to the error messages or the logs for troubleshooting.
