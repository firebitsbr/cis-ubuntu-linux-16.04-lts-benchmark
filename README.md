# CIS-Ubuntu-Linux-16.04-LTS-Benchmark
Ansible role that configures Ubuntu Linux 16.04 LTS to CIS Benchmark

## Requirements
Ansible 2.3+

## Install Ansible
```
sudo apt-get update && sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update && sudo apt-get install ansible
```

## Download Role From GitHub
```
git clone https://github.com/paxdominicus/cis-ubuntu-linux-16.04-lts-benchmark.git roles/cis-ubuntu-linux-16.04-lts-benchmark
```

## Create Playbook
```
cat >>  playbook.yml << 'EOF'
---
- hosts: all
  roles:
    - cis-ubuntu-linux-16.04-lts-benchmark
EOF
```

## Configure Playbook
```
sudo nano roles/cis-ubuntu-linux-16.04-lts-benchmark/defaults/main.yml
```

## Run Playbook
```
sudo ansible-playbook -b -i "localhost," -c local playbook.yml
```
