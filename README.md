# Ansible Playbook: Create Golden Image of LXD Container

This Ansible playbook automates the process of creating a golden image of a LXD container and publishing the container as an image.

## Prerequisites

Before running this playbook, ensure you have the following prerequisites set up:

### Ansible installed 

### Inventory File: 

If you won't use localhost as the host, create an inventory.ini file with the necessary host configurations. Refer to the Ansible documentation for more information on creating an inventory file.

### Ansible Configuration: 

You may need to set up an ansible.cfg file with the following configurations:

- host_key_checking 
- ansible_ssh_private_key_file 
- remote_user 

Adjust these configurations based on your environment and requirements.

### Variables File: 

Set up a variables.yaml file with the following variables:

- new_container: Name of the new LXD container.
- image_alias: Alias for the published LXD container image.
- username1: Name of first user created.
- sudo_users: List of users with sudo privileges.
- non_sudo_users: List of users without sudo privileges.
- su_group_users: List of users belonging to the 'su' group.
- root_pass: Root password for the LXD container.

### Usage

To use this playbook, follow these steps:

1. Ensure you have met all the prerequisites mentioned above.

2. Clone this repository to your local machine:

```bash
git clone https://github.com/audreyper/golden-image.git

#### Navigate to the directory containing the playbook:

```bash
cd <playbook-directory>

#### Run the playbook:

```bash
ansible-playbook playbook.yml -i inventory.ini

