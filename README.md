# Ansible Project: SRE Dashboard and Alerting with Grafana, Prometheus, and Node Exporter

## Table of Contents

- [ProjectOverview](#overview)
- [Prerequisites](#prerequisites)
- [RolesOverview](#Overview)
- [Usage](#Usage)

## ProjectOverview

This Ansible project automates the setup and configuration of a Site Reliability Engineering (SRE) Dashboard and Alerting system. The project uses Ansible roles to deploy Grafana for visualization, Prometheus for monitoring, and Node Exporter for collecting system metrics on target servers. This integrated setup enables you to monitor infrastructure and application health effectively.


## Prerequisites

Before using this role, ensure that you have the following prerequisites in place:

1. Ansible installed on your control node.

2. SSH access to the target servers with the necessary permissions.

3. A compatible Linux distribution on your target AWS Linux servers.

4. Correctly configured AWS Dynamic Inventory.

5. AWS credentials or appropriate IAM roles for accessing EC2 instances.

# RolesOverview

This Ansible role includes tasks for:

- Installing and configuring Grafana for visualizing data and metrics.
- Installing and configuring Prometheus as the monitoring and alerting toolkit.
- Installing and configuring Node Exporter for collecting server metrics.

By using this role, you can streamline the setup and management of monitoring tools in your infrastructure.

## Ansible Role for Configuring Grafana, Prometheus, and Node Exporter

This Ansible role simplifies the process of configuring Grafana, Prometheus, and Node Exporter on your target servers. It is designed to automate the installation and setup of these monitoring tools, enabling you to monitor infrastructure and application health efficiently.
    - 
  
## Usage

Follow these steps to set up the SRE Dashboard and Alerting system using this Ansible project:

1. Clone or download this repository to your Ansible control node.

2. Review and customize the inventory file (`inventory.ini`) to specify the target servers.

3. Edit the playbook (`sre_dashboard.yml`) to match your environment's requirements and add the roles for Grafana, Prometheus, and Node Exporter.
4. Include this role in your playbook and specify the role variables as needed.

5. Run the playbook using the following command:

   ```bash
   ansible-playbook -i inventory.ini sre_dashboard.yml

