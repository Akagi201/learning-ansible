# Ansible Scaffold

## Structure

```
/group_vars - inventory group vars
/host_vars - inventory host vars
/roles - playbook roles
/site.yml - the playbook logic
/hosts - inventory file
/ansible.cfg - ansible config file
```

## Run

```
ansible all -i ./hosts -a "echo hello"
```

## Refs
* [Ansible best practice](http://docs.ansible.com/ansible/playbooks_best_practices.html)
