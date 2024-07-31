# Ansible Project for Java Web Application Deployment

This project contains an Ansible playbook and associated configuration files to automate the deployment of a Java web application on an Ubuntu server.

## Project Structure

```
ansible_project/
├── README.md            
├── ansible.cfg          
├── inventory.cfg        
├── main.yaml            
└── templates/   
    ├── application.properties.j2  
    └── pom.xml.j2              
```

## Prerequisites

- Python on your machine

- Ansible installed on your machine.

- SSH access to the target Ubuntu server.

- Git installed on the target server.

## Usage

1. Clone this repository to your local machine.

```
git clone https://github.com/yourusername/ansible_project.git
cd ansible_project
```

2. Create the inventory.cfg file with your target server's IP address, SSH user, and path to your SSH private key.

```
[all]
your_server_ip ansible_user=your_ssh_user ansible_ssh_private_key_file=path_to_your_private_key
```

3. Update the main.yaml playbook with appropriate values for your environment. Ensure the `app_host` and `rabbitmq_host variables` are set correctly for your environment.

4. Run the playbook using the following command:

```
ansible-playbook main.yaml -b
```
