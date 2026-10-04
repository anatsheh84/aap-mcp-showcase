# AAP MCP showcase playbooks

Small, readable playbooks for demonstrating the Ansible Automation Platform MCP server:
an AI agent launches them through AAP job templates, reads the results and explains them.

| Playbook | Target | What it does |
|---|---|---|
| `rhel_health_report.yml` | RHEL | Read-only: uptime, load, memory, disk, failed services, pending updates |
| `windows_health_report.yml` | Windows | Read-only: uptime, memory, disk, stopped automatic services, last patches, pending reboot |
| `rhel_webserver.yml` | RHEL | Installs and starts a web server with a status page, then verifies it answers |
| `rhel_restart_service.yml` | RHEL | Restarts one named service and reports its state |

They run against whatever hosts the job template's inventory and limit select; nothing in
this repository is environment-specific and it holds no secrets.

Source of truth: the `showcase/` directory of the app-orchestrator project, published by
`make mcp-showcase`.
