** POC Developer Tasks (low) - Windows or Linux: **

1. Connectivity test:
Write a playbook to test the connectivity to the defined target host using the ping module

2. Creating a directory:
Write a playbook to create two directories in your user’s home directory named “PoC1” and “PoC2”

3. Gathering system information:
Write a playbook to gather system information about the target host and save it to a file “system_facts.json” in JSON format in the directory “PoC1”.
In this same playbook, also save these system facts to another file “system_facts.yaml” in YAML format in the directory “PoC2”

4. Copy files:
Write a playbook to copy the contents of “PoC1” and “PoC2” into a new folder “PoC3”


5. Web server
Write a playbook to install and enable the correct web server package for the target OS
As the main index page, the contents should be the inventory hostname of this server along with the IP address displayed for any visitor.


** PoC Developer Tasks (complex) **

1. Provision a vCenter VM
Write a playbook to provision a VM with the following details (where indicated, simply use the variable name and not a real value):
name: ansible-poc-vm
vcenter hostname: {{ vcenter_hostname }}
vcenter username: {{ vcenter_username }}
vcenter password: {{ vcenter_password }}
datacenter: {{ vcenter_datacenter }}
cluster: {{ vcenter_cluster }}
template to clone from: {{ vcenter_template }}
folder: {{ vcenter_folder }}
memory: same as the current host (may require a task to determine first)

2. Take a snapshot of the VM just provisioned
