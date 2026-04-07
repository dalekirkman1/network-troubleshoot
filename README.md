# IOS-XE Health Check

Ansible role that performs state validation and troubleshooting
across Cisco IOS-XE devices, covering system info, CPU, memory,
interfaces, SFP transceivers, CDP topology, OSPF, BGP, and logs.
A timestamped text report is saved locally per device after each run.

## Requirements

### Python packages
```bash
pip install -r requirements.txt
```

### Ansible collections
```bash
ansible-galaxy collection install -r requirements.yml
```

## Usage

```bash
# Run all sections against production inventory
ansible-playbook site.yml

# Run specific sections by tag
ansible-playbook site.yml --tags bgp,ospf

# Target a single device
ansible-playbook site.yml --limit router1

# Use the lab inventory
ansible-playbook site.yml -i inventory/lab/hosts.yml

# Prompt for vault password
ansible-playbook site.yml --ask-vault-pass
```

## Role Variables

All defaults are in `roles/ios_xe_health_check/defaults/main.yml`.

| Variable            | Default      | Description                              |
|---------------------|--------------|------------------------------------------|
| cpu_lines_to_show   | 7            | Lines of CPU process output to display   |
| mem_lines_to_show   | 15           | Lines of memory output to display        |
| log_lines_terminal  | 20           | Syslog lines printed to terminal         |
| log_lines_report    | 15           | Syslog lines written to report file      |
| standard_mtu        | "1500"       | MTU value considered normal              |
| ospf_full_state     | "FULL"       | Expected OSPF adjacency state string     |
| report_dir          | "./reports/" | Output directory for report files        |

## Available Tags

| Tag          | Sections covered                        |
|--------------|-----------------------------------------|
| system       | Software version, uptime, reload reason |
| health       | Control-processor status                |
| cpu          | CPU processes (sorted 5sec)             |
| memory       | Memory statistics (sorted)              |
| interfaces   | Interface status, errors, MTU           |
| transceivers | SFP optical diagnostics                 |
| topology     | CDP neighbor discovery                  |
| ospf         | OSPF neighbor state                     |
| bgp          | BGP peering state                       |
| logs         | Recent syslog messages                  |
| report       | Generate local text report              |

## Credentials

Store credentials encrypted in `group_vars/all/vault.yml`:

```bash
ansible-vault encrypt group_vars/all/vault.yml
```
