# Role: nxos_troubleshoot

Performs health data collection and reporting across Cisco NX-OS devices.

See the top-level README.md for full usage instructions.

## Task Files

| File                  | Sections | Tags                         |
|-----------------------|----------|------------------------------|
| 00_setup.yml          | —        | setup                        | 
| 01_system_info.yml    | 1        | system, identity, facts      | 
| 02_uptime.yml         | 2        | uptime, system               | 
| 03_platform_health.yml| 3        | health, platform             | 
| 04_cpu_top.yml        | 4        | cpu, health                  |
| 05_memory.yml         | 5        | memory, health               | 
| 06_interface_status.yml | 6      | interfaces, status           | 
| 07_interface_health.yml | 7      | interfaces, health, mtu      | 
| 08_sfp_diagnostics.yml | 8       | interfaces, optics, sfp      | 
| 09_cdp_topology.yml   | 9        | topology, cdp, neighbors     | 
| 10_ospf_neighbors.yml | 10       | routing, ospf                | 
| 11_bgp_peering.yml    | 11       | routing, bgp                 | 
| 12_recent_logs.yml    | 12       | logs, health                 | 
| 99_write_report.yml   | 13       | report                       | 
