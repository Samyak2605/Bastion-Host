# Bastion Host Setup on AWS

## 📌 Overview
This project demonstrates how to securely access a private EC2 instance using a Bastion Host (jump server) on AWS.

## ☁️ Infrastructure

- **Bastion Host**: Public EC2 (Ubuntu 24.04) with SSH access.
- **Private Server**: Private EC2 (Ubuntu 24.04) accessible only through the Bastion host.

## 🔒 SSH Config

Located at `~/.ssh/config`:

```ssh
Host bastion
    HostName 13.48.13.51
    User ubuntu
    IdentityFile /Users/samyakmittal/Downloads/Bastion\ Host.pem

Host private-server
    HostName 172.31.24.75
    User ubuntu
    IdentityFile /Users/samyakmittal/Downloads/private-key.pem
    ProxyJump bastion
This is the project link: https://roadmap.sh/projects/bastion-host
