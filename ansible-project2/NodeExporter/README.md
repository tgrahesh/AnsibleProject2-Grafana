# Node Exporter Ansible Role

This Ansible role automates the installation and configuration of Node Exporter, a Prometheus exporter for server-level hardware and operating system metrics. Node Exporter collects various system metrics that can be scraped by Prometheus, facilitating server monitoring.

## Overview

This Ansible role includes tasks for:

- Downloading the Node Exporter release archive.
- Calculating and displaying the SHA-256 checksum.
- Extracting the Node Exporter release archive.
- Copying the Node Exporter binary to `/usr/local/bin`.
- Rendering Node Exporter configuration from a Jinja2 template.
- Replacing the content of the systemd service unit file.
- Reloading systemd to apply changes.
- Enabling the Node Exporter service.
- Restarting Prometheus to include Node Exporter metrics.

By using this role, you can automate the setup of Node Exporter for server monitoring.

## Role Variables

This role allows customization through variables. The following variables are available for configuration:

- `n_user`: The name of the 'node_exporter' user.
- `node_url`: The URL to download the Node Exporter release archive.

You can customize these variables in your playbook to match your environment's requirements.

## Prerequisites

Before using this role, ensure that you have the following prerequisites in place:

1. Ansible installed on your control node.

2. SSH access to the target servers with the necessary permissions.

3. A compatible Linux distribution on your target servers (e.g., Ubuntu, CentOS).

4. Correctly configured AWS Dynamic Inventory or custom inventory.

5. AWS credentials or appropriate IAM roles for accessing EC2 instances (if applicable).

## Usage

1. Clone or download this repository to your Ansible project directory.

2. Include this role in your playbook and specify the role variables as needed.
3. Run the playbook using the following command:
    ansible-playbook -i inventory.ini your_playbook.yml
