# SSH Key Authentication Setup for Linux Targets

This Ansible playbook automates the setup of SSH key authentication on Linux targets. It performs the following tasks:

## Prerequisites
- Ansible installed on the control machine.
- Inventory file (`hosts`) properly configured with target hosts.
- `group_vars/credentials` file containing necessary variables.
- `exported_keys` directory should exist.

## Usage
1. Clone the repository:
    ```bash
    git clone git@github.com:Jeremy-Sch/ansible-ssh-setup.git
    ```
    ```bash
    cd ansible-ssh-setup
    ```
2. Update the ansible-vault file `group_vars/credentials` with your configuration.
 ```bash
ansible-vault create group_vars/credentials
ansible-vault view  group_vars/credentials
ansible_user: root
ssh_user: automation
 ```

4. Create the  `exported_keys` directory:
   ```bash
    mkdir exported_keys
    ```

5. Execute the playbook using the following command:
   ```bash
   ansible-playbook -i playbooks/ssh-setup.yml
   ```

