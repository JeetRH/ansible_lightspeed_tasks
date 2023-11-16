Write playbooks to satisfy the following requirements. Use a host group named poc_hosts for all tasks below.

Also after writing each playbook, please answer the following questions. Put the answers as comments on top of the file. A comment in yaml starts with #:

How many times did you have to leave your VSCode to complete this?
List all the sources you used to complete this task?
How long did it take to complete this task?


Problem set 1:
** POC Developer Tasks (low): **

Name the playbook as - m_1.yml
Connectivity test: 
use a module to verify connectivity to the defined target 
use the ping module to accomplish this

Name the playbook as - m_2.yml
Creating directories:
create two directories in your user’s home directory 
the directories should be named “PoC1” and “PoC2”
use mode 0775
Use owner and group as user1

** POC Developer Tasks (medium)**

Name the playbook as - m_3.yml
Web server: 
install and enable the correct web server package for the target OS
As the main index page, use the following for content when a visitor hits this page:
inventory hostname of this server 
IP address displayed for any visitor.

** PoC Developer Tasks (complex) **

Name the playbook as - m_4.yml (solve both 1 and 2 in the same playbook)
Provision a vCenter VM with the following details: (where indicated, simply use the variable name and not a real value):

name: ansible-poc-vm 
vCenter hostname is {{ vcenter_hostname }} 
vCenter username is {{ vcenter_username }} 
vCenter password is {{ vcenter_password }} 
do not validate certs 
Datacenter is {{ vcenter_datacenter }} 
Cluster is {{ vcenter_cluster }} 
template to clone from: {{ vcenter_template }} 
Folder to store {{ vcenter_folder }} 
memory: same as the current host (may require a task to determine first)
create a disk of 10 gb
make the state as powered on
tag the VM with the following tags: tag1 -> poc, tag2 -> ansible

Also, take a snapshot of the VM just provisioned:
put it in the {{ vcenter_folder }} 
name it as ansible-poc-snapshot



Write playbooks to satisfy the following requirements. Use a host group named poc_hosts for all tasks below.

Also after writing each playbook, please answer the following questions. Put the answers as comments on top of the file. A comment in yaml starts with #::

How many times did you have to edit the suggested code?
Did you ever have to leave your VSCode to complete this task?
How long did it take to complete this task?

Problem set 2:
** POC Developer Tasks (low): **
Name the playbook as - ls_1.yml
Create files: 
create a file with content “poc1 text” in a file named poc1.txt
create a file with content “poc2 text” in a file named poc2.txt

Name the playbook as - ls_2.yml
Copy Files
copy the file poc1.txt into a new folder “PoC3”
copy the file poc2.txt into a new folder “PoC3”

** POC Developer Tasks (medium)**

Name the playbook as - ls_3.yml
Gathering system information: 
gather system information about the target host 
save it to a file “system_facts.json” in JSON format in the directory “PoC1”
also save these system facts to another file “system_facts.yaml” in YAML format in the directory “PoC2”

** PoC Developer Tasks (complex) **

Name the playbook as - ls_4.yml (solve both 1 and 2 in the same playbook)
Provision an AWS EC2 VM with the following details (where indicated, simply use the variable name and not a real value):

Name it as ansible-poc-aws 
Access key is {{ aws_access }} 
Secret key is {{ aws_secret }} 
Ssh key is {{ ssh_key_name }} 
Instance type should be {{ aws_instance_type }}
Security group is {{ aws_security_group }}
Image to use {{ aws_image_id }} 
AWS Region is {{ aws_region }}
VPC Subnet Id is {{ aws_vpc }}
Enable 2 cores and 2 threads per core
Public ip should be enabled
state should be present
tag the VM with the following tags: tag1 -> poc, tag2 -> ansible

Also, take a snapshot of the VM just provisioned

Volume Id: {{ aws_volume_id }}
AWS Region: {{ aws_region }}
Description: ansible-poc-snapshot

