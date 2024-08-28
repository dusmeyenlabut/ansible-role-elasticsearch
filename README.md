# Elasticsearch Cluster Setup with Ansible

This Ansible role is used for setting up an Elasticsearch 8.x cluster.

## Prerequisites

Before running this role, passwordless SSH access must be set up for a user with root privileges. By default, the user is specified as `root`, but this can be changed in the `hosts` file.

### Steps to Set Up Passwordless SSH Login on Linux

To configure passwordless SSH login, follow these steps:

1. Generate an SSH key pair on the local machine:
   
   ```bash
   ssh-keygen -t rsa -b 4096
   ```
2. Copy the public key to the remote machine:
   
   ```bash
   ssh-copy-id root@remote_host
   ```
3. Verify passwordless SSH login by connecting to the remote machine:

   ```bash
   ssh root@remote_host
   ```

### Running the Ansible Playbook
Once the prerequisites are set up, you can run the Ansible playbook to set up the Elasticsearch cluster using the following command:

   ```bash
   ansible-playbook playbook.yaml -i hosts -kK
   ```