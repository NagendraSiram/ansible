# ansible commands

> ansible-doc -l | more *(list all modules installed)*

> ansible-doc -s yum *(to learn about yum module)*

> ansible appservers -m ping

> ansible all -m ping -o *(output in single line)*

> ansible all -m shell -a "uname -a;df -h"

> ansible all -m shell -a "uname -a;df -h" -v *(for verbose)*

> ansible appservers -m service -a "name=httpd  state=started" -s *(-s is to use root user on target machine)*

> ansible all -m copy -a "src=/tmp/testfile dest=/tmp/testfile" -s *(do it as root)*

> ansible -i /root/myhostfile all -m shell -a "uptime"

> ansible -i /root/myhostfile all -l onlyOneServer -m shell -a "uptime" *(limit to one host)*

## playbook commands

> ansible-playbook myplaybook.yml

> ansible-playbook --help

> ansible-playbook example.yml --tags "configuration,packages"

> ansible-playbook example.yml --skip-tags "packages"

> ansible-playbook example.yml --tags "configuration,packages" --list-tasks *(to list which tasks gets executed)*
