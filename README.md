# Ec2-creation-and-manage-using-Ansible-playbook

[![Build](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

---

## Description 

Simple ansible playbook for creating a amazon Ec2 with all required resoruces.  

----
## Pre-Requests
- Need to install ansible2 on Master node to run
- python3
- python3-pip
- boto3
- awscli with latest version
-----

### Ansible installation 

```sh
amazon-linux-extras install epel -y
amazon-linux-extras install ansible2 -y
yum install python3
yum install python3-pip
pip install awscli --upgrade
ansible-galaxy connection install amazon.aws -y
pip3 install boto3
pip3 install botocore
```

### Behind the code : hosts file
```sh
~]$ cat hosts
localhost ansible_connection=local ansible_python_interpreter=/usr/bin/python3
```
> You need to verify the localhost ansible is now able to communicate with python3. For verify

```sh
~]$ ansible -i hosts localhost -m setup | grep "ansible_python_version"
        "ansible_python_version": "3.7.10"
 ```
