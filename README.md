# Ansible deployment for Passenger

## 0. Current Stats

[![Build Status](https://travis-ci.org/configuresystems/ansible-passenger.svg?branch=master)](https://travis-ci.org/configuresystems/ansible-passenger)

|    Name         |    Description            |
| --------------- | ------------------------- |
| Version         | 1.0                       |
| Updated         | 03.24.2015                |
| Ansible Version | 1.8.4                     |
| Author          | Johnny Martin             |
| Website         | http://configure.systems/ |
| License         | MIT                       |


## 1. QuickStart

```bash
git clone https://github.com/configuresystems/ansible-passenger.git roles/ansible-passenger
# Create a playbook file to use, there's a sample one in tests/test.yml
# Create a group_vars or update the default values in defaults/main.yml
ansible-playbook -i path/to/inventory ansible-playbook.yml
```

    
## Table of contents

- [1. QuickStart](#1-quickstart)
- [2. Overview](#2-overview)
- [3. Requirements](#3-requirements)
  - [3.1 Ubuntu](#31-ubuntu)
  - [3.2 Compile from Source](#32-compile-from-source)
- [4. Usage](#4-usage)
- [5. Passenger Control](#6-passenger-control)
  - [5.1 Version](#61-version)
  - [5.2 Root](#62-root)


## 2. Overview

An Ansible playbook to automate the installation of passenger.

This role is intended to be used in conjuction with ansible-apache2, located
here:

https://github.com/configuresystems/ansible-apache2.git

## 3. Requirements

Ansible installed on the local machine.

#### 3.1 Ubuntu

```bash
pip install ansible
```

#### 3.2 Compile from Source

```bash
git clone git://github.com/ansible/ansible.git --recursive
cd ./ansible
source ./hacking/env-setup
```

## 4. Usage

1. `git clone http://github.com/configuresystems/ansible-passenger`
   or update the 'defaults/main.yml' file
3. run the Ansible playbook, the fastest way is:

```bash
ansible-playbook ansible-passenger.yml
```

### 5. Passenger Control

#### 5.1 Version

```bash
sudo passenger-config --version
```

#### 5.2 Root

```bash
sudo passenger-config --root
```
