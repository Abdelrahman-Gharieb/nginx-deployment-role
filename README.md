# Ansible Role: NGINX Web Server:
An Ansible role that automates the installation, configuration, and management of the **NGINX** web server on **Ubuntu Linux** distributions.

## Requirements:
No special pre-requisites beyond a target host running Ubuntu Linux and standard Ansible SSH connectivity.

## Role Variables:
The available variables and their default variables are defined in `defaults/main.yml`:

| Variable | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| `nginx_port` | Integer | The listening port for the NGINX HTTP server. | `80` |
| `nginx_service_state` | String | Desired state of the NGINX service (`started`, `stopped`). | `started` |
| `nginx_service_enabled` | Boolean | Whether the NGINX service should start automatically on boot. | `true` |

## Dependencies:
This role does not depend on any external Ansible Galaxy roles.

## Example Playbook:

To use this role in your playbook, pass it as follows:

```yaml
- hosts: webservers
  become: yes
  roles:
    - role: Abdelrahman-Gharieb.nginx_deployment_role
      vars:
        nginx_port: 80
```
## Directory Structure:
```text
nginx-deployment-role/
├── defaults/          # Default variables for the role
├── handlers/          # Handlers for service restarts/reloads
├── meta/              # Role metadata and author information
├── tasks/             # Main execution tasks (installation, configuration)
├── templates/         # Jinja2 templates (e.g., virtual host configs)
├── tests/             # Test playbooks and inventory for verification
├── vars/              # Additional variables (if applicable)
└── README.md          # Role documentation
```
## License:
BSD

## Author Information:
Created by **Abdulrahman Gharieb** (DevOps Engineer).
GitHub: [ **@Abdelrahman-Gharieb** ].
