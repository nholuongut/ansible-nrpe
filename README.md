# nrpe
![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

## Requirements

### Roles

- [nholuong.ansible_lib](https://galaxy.ansible.com/nholuong/ansible_lib)

### Collections

- community.general


## Variables

Review defaults and examples in vars.


## Workflow

1) Install the role and collections

```
shell> ansible-galaxy role install nholuong.nrpe
shell> ansible-galaxy collection install community.general
```

2) Change variables, e.g. vars/main.yml

```
shell> editor nholuong.nrpe/vars/main.yml
```

3) Create playbook and inventory

```
shell> cat nrpe.yml
---
- hosts: webserver
  roles:
    - nholuong.nrpe
```

```
shell> cat hosts
[webserver]
<webserver-ip-or-fqdn>
[webserver:vars]
ansible_connection=ssh
ansible_user=freebsd
ansible_become=yes
ansible_become_method=sudo
ansible_python_interpreter=/usr/local/bin/python3.6
ansible_perl_interpreter=/usr/local/bin/perl
```

4a) Check syntax

```
shell> ansible-playbook nrpe.yml --syntax-check
```

4b) Display variables

```
shell> ansible-playbook nrpe.yml -e nrpe_debug=true -t nrpe-debug
```

4c) Install packages

```
shell> ansible-playbook nrpe.yml -e nrpe_install=true -t nrpe-packages
```

4d) Dry-run and show changes

```
shell> ansible-playbook nrpe.yml --check --diff
```

5) Run the playbook if all seems to be right

```
shell> ansible-playbook nrpe.yml
```

6) Plugins (TBD)
		

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
