# Grafana Ansible Role

This Ansible role automates the installation and configuration of Grafana, a popular open-source platform for monitoring and observability. Grafana provides features for creating dashboards, visualizing metrics, and integrating with various data sources.

## Overview

This Ansible role includes tasks for:

- Adding the Grafana GPG key to the keyring.
- Adding the Grafana repository to sources.list.
- Updating the APT cache (for Debian-based systems).
- Installing Grafana.
- Enabling the Grafana service.

By using this role, you can automate the setup of Grafana for dashboard creation and metric visualization.

## Role Variables

This role allows customization through variables. The following variables are available for configuration:

- `grafana_gpg_key`: The command to add the Grafana GPG key to the keyring.
- `grafana_repo`: The command to add the Grafana repository to sources.list.

Customize these variables in your playbook to match your environment's requirements.

## Prerequisites

Before using this role, ensure that you have the following prerequisites in place:

1. Ansible installed on your control node.

2. SSH access to the target servers with the necessary permissions.

3. A compatible Linux distribution on your target servers.

4. Correctly configured AWS Dynamic Inventory.

5. AWS credentials or appropriate IAM roles for accessing EC2 instances.

## Usage

1. Clone or download this repository to your Ansible project directory.

2. Include this role in your playbook and specify the role variables as needed.
3. Run the playbook using the following command:
      ansible-playbook -i inventory.ini your_playbook.yml



