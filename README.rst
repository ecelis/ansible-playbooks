Ansible playbooks
=================

``bash
ansible-playbook -i hosts <playbook.yml> [--verbose]
``

Manage only one service

``bash
ansible -i hosts -m <service|systemd> -a 'name=<service>
state=<started|stoped|restarted>' -b <target>
``

To schedule playbooks execution, use crontab.

``bash
crontab -e
# Add the line below
0 19 * * 5 ansible-playbook -i hosts <playbook.yml>
``
