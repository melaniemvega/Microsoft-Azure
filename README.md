## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

<figure><img src="/Diagrams/Diagram.PNG"><figcaption></figcaption></figure>

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the install-elk.yml file may be used to install only certain pieces of it, such as Filebeat.

install-elk.yml

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting unwanted traffic to the network.
- Availability for traffic so servers do not go down and to control traffic
- Jumpbox for a secure backend access

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the log files and system metrics.
- Filebeat helps generate and organize giles to send to Logstash and Elesticsearch. It specifially logs inforamiton about the file system, including which files hae chaneges and when.
- Metricbeat monitors the metrics of the DVWA virtual machines.

The configuration details of each machine may be found below.

| Name       | Function      | IP Address | Operating System          |  
|------------|---------------|------------|---------------------------|
| Jump Box   | Gateway       | 10.0.0.7   | Linux - Ubuntu 18.04-LTS  |
| Elk Server | Cloud Monitor | 10.1.0.4   | Linux - Ubuntu 18.04-LTS  |
| Web-1      | Web Server    | 10.0.0.5   | Linux - Ubuntu 18.04-LTS  |
| Web-2      | Web Server    | 10.0.0.6   | Linux - Ubuntu 18.04-LTS  |
| DVWA-VM3   | Web Server    | 10.0.0.1   | Linux - Ubuntu 18.04-LTS  |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jumpbox, Elk Server and Load Balancer machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- Jumpbox (40.117.145.95)
- Elk Server (52.237.160.182)
- Load Balaner (40.121.135.134)

Machines within the network can only be accessed by _____.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_

A summary of the access policies in place can be found in the table below.

| Name                           |  Publicly Accessible | Allowed IP Addresses              |
|--------------------------------|----------------------|-----------------------------------|
| Jump Box - Port 22             | Yes                  | Personal IP address               |
| Elk Server - Port 5601         | Yes                  | 10.1.0.4                          |
| Web Server - Port 22           | No                   | 10.0.0.4                          |
| DVWA Load Balancer - Port 80   | Yes                  | 71.201.212.82 Local home network  |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

<figure><img src="Images/Docker-ps.PNG"><figcaption></figcaption></figure>

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
