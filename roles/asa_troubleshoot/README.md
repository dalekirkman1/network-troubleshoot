# Role: asa_health_snapshot

Performs health data collection and reporting across Cisco ASA devices. 

See the top-level README.md for full usage instructions.

## Overview

This role connects to Cisco ASA firewalls, runs a curated set of `show` commands, normalises the raw CLI output with Jinja2, and exposes concise facts per device that can be rendered into a troubleshooting or health report. It is organised into numbered sections that mirror a typical troubleshooting workflow (identity, uptime, platform health, interfaces, topology, VPN, and failover).

## Task Files

| File                          | Sections | Tags                      |
|-------------------------------|----------|---------------------------|
| 01_system_info.yml            | 1        | identity, health          |
| 02_uptime.yml                 | 2        | health                    |
| 03_platform_health.yml        | 3        | health                    |
| 04_cpu_top_processes.yml      | 4        | cpu, health               |
| 05_memory_statistics.yml      | 5        | memory, health            |
| 06_interface_status.yml       | 6        | interfaces, health        |
| 07_interface_health.yml       | 7        | interfaces, health        |
| 08_transceiver_equivalent.yml | 8        | interfaces, health        |
| 09_topology.yml               | 9        | topology, routing         |
| 10_routing_state.yml          | 10       | routing                   |
| 11_flow_nat_state.yml         | 11       | nat, flows, health        |
| 12_recent_logs.yml            | 12       | logs, health              |
| 13_vpn_state.yml              | 13       | vpn, health               |
| 14_failover_state.yml         | 14       | ha, health                |
| 99_write_report.yml           | 15       | report                    |
