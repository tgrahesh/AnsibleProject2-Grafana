# Prometheus Ansible Role

This Ansible role is designed to automate the installation and configuration of Prometheus, an open-source monitoring and alerting toolkit, on your target servers. It streamlines the setup and management of Prometheus, allowing you to collect and visualize metrics from various sources.

## Overview

This Ansible role includes tasks for:

- Adding 'prometheus' and 'node_exporter' users.
- Creating necessary directories and ownership.
- Downloading the Prometheus release archive.
- Calculating and displaying the SHA-256 checksum.
- Extracting the Prometheus release archive.
- Copying Prometheus binaries to `/usr/local/bin`.
- Copying Prometheus consoles and libraries.
- Replacing Prometheus configuration files.
- Setting up Prometheus as a system service.

By using this role, you can efficiently configure Prometheus for monitoring your infrastructure.

## Role Variables

The role allows customization through variables. The following variables are available for configuration:

- `p_user`: The name of the 'prometheus' user.
- `n_user`: The name of the 'node_exporter' user.
- `prometheus_url`: The URL to download the Prometheus release archive.

Customize these variables in your playbook to match your environment's requirements.

## Prerequisites

Before using this role, ensure that you have the following prerequisites in place:

1. Ansible installed on your control node.

2. SSH access to the target servers with the necessary permissions.

3. A compatible Linux distribution on your target servers.

4. Correctly configured AWS Dynamic Inventory

5. AWS credentials or appropriate IAM roles for accessing EC2 instances.

## Usage

1. Clone or download this repository to your Ansible project directory.

2. Include this role in your playbook and specify the role variables as needed. Here's an example playbook:

   ```yaml
   - name: Configure Prometheus
     hosts: your_target_hosts
     become: yes

     roles:
       - role: prometheus
         vars:
           p_user: prometheus
           n_user: node_exporter
           prometheus_url: https://example.com/prometheus-2.47.1.linux-amd64.tar.gz
   2. Run the playbook using the following command:
   ansible-playbook -i inventory.ini your_playbook.yml

