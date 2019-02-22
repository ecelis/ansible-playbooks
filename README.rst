Ansible playbooks
=================

``bash
ansible-playbook -i hosts <playbook.yml> [--verbose]
``

To schedule playbooks execution, use crontab.

``bash
crontab -e
# Add the line below
0 19 * * 5 ansible-playbook -i hosts <playbook.yml>
``
