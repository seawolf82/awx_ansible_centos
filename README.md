# awx_ansible_rocky8

Before to run the script, install on remote host this package: python39 
To do this run: dnf install python39 -y

This ansible script install on remote machine The awx project, To install run:

ansible-playbook -vv -i hosts site.yaml

To uninstall run:

ansible-playbook -vv -i hosts deprovision.yaml

Adding Tags to permit run only specific task of playbook

Tags:

upgrade package awx awx_uninstall awx_repo

For example, to launch only task regarding upgrade os, run:

ansible-playbook -vv --tags "upgrade" -i hosts site.yaml
