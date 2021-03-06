# Ansible Workshop

Hi! Welcome to the **Ansible Workshop**. In this repository you can find variety of exercises that would help you to strengthen your Ansible skills.

## Exercise 3

> Run a playbook that downloads and installs Notepad++ on a remote windows machine

## Solution

- Update the inventory file with your Windows host IP: `sed -i -e 's/10.0.0.2/IPADDRESS/g' inventory.yml`
- `ansible-playbook playbook.yml -i inventory.yml -e "ansible_user=Administrator ansible_password=123Cyber" -v`
- -v stands for verbose, so we can see the output of our commands (and debug if necessary).
- -i stands for inventory, we point to a specific file where our hosts are defined.
- -e stands for extra vars, where you can specify variables to use inside the playbook. `ansible_user` and `ansible_password` are **unique variables** used to login to Windows machines with username and password.

## Next Step

Finished with this exercise? go to [Exercise 4](../exercise-4)
