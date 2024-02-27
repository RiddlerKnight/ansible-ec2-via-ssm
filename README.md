# Getting start with Ansible init ec2

## Prerequisite

1. create s3 bucket even if you didn't have any file to update to target instance.

2. login you aws session on your pc or ansible execution host.

## steps

1. install awscli and session-manager plugin

```bash

curl "https://s3.amazonaws.com/session-manager-downloads/plugin/latest/ubuntu_64bit/session-manager-plugin.deb" -o "session-manager-plugin.deb"
sudo dpkg -i session-manager-plugin.deb
```

2. install python and ansible

```bash
# update dp on your machine
sudo apt update
sudo apt upgrade

sudo add-apt-repository ppa:deadsnakes/ppa -y
sudo apt update
sudo apt install python3.11

# check
python3.11 --version
```

3. install boto3 (aws python lib)

```bash
pip install boto3
```

4. download community.aws

```bash
ansible-galaxy collection install community.aws
```

5. execute

```bash
ansible-playbook -i inventory.aws_ec2.yaml playbook.yaml
```

## New area concern

1. a
