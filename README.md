# Ansible Role: Prometheus
An ansible role which setup Prometheus Server for your awesome monitoring setup.

## Requirements

There is no particular requirment for running this role. This supports below listed OS platforms
- **RedHat** or **CentOS** 6 and 7
- **Debian**

## Role Variables
The role variables are defined in the **[defaults](https://github.com/iamabhishek-dubey/ansible-role-prometheus/tree/master/defaults)**. So there is not so many variables you just have to pass the prometheus version.

### Mandatory Variables
There is no mandatory variables needed.

### Optional Variables

|**Variable**|**Default Value**|**Description**|
|------------|-----------------|---------------|
|version|2.3.2|Prometheus server version|
|prometheus_ip|0.0.0.0|Default IP which binds with Prometheus|
|prometheus_port|9090|Default port number on which Prometheus listens|

## Dependencies
None :-)

## Example Playbook
Here is an example playbook for running this role
```yaml
---
- hosts: prometheus
  user: test-user
  become: true
  roles:
    -  iamabhishek_dubey.ansible_role_prometheus
```
For inventory you can create a host file in which you can define your server ip, For example:-
```ini
[prometheus]
10.1.1.100
```

You can simply use this role by using this command
```shell
ansible-playbook -i hosts site.yml
```
## License

GNU

## Author Information

This role is written and maintained by [Abhishek Dubey](https://github.com/iamabhishek-dubey). If you have any queries and sugesstion, please feel free to reach.
