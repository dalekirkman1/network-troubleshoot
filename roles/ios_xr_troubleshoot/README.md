# Role: ios_xr_health_check

Performs health data collection and reporting across Cisco IOS XR devices.

See the top-level README.md for full usage instructions.

## Task Files

| File                     | Sections | Tags                      |
|--------------------------|----------|---------------------------|
| 01_system_info.yml       | 1        | identity, health          | 
| 02_uptime.yml            | 2        | health                    | 
| 03_platform_health.yml   | 3        | health                    | 
| 04_cpu_top_processes.yml | 4        | cpu, health               | 
| 05_memory_statistics.yml | 5        | memory, health            | 
| 06_interface_status.yml  | 6        | interfaces, health        | 
| 07_interface_health.yml  | 7        | interfaces, health        | 
| 08_transceiver_equivalent.yml | 8   | health, optics            | 
| 09_topology.yml          | 9        | topology, neighbors       | 
| 10_routing_state.yml     | 10       | routing                   |
| 11_flow_state.yml        | 11       | flows, health             | 
| 12_recent_logs.yml       | 12       | logs, health              | 
| 13_alarms_faults.yml     | 13       | health, alarms            | 
| 14_lpts_control_plane.yml| 14       | control-plane, lpts, health | 
| 15_qos_policy.yml        | 15       | qos                       | 
| 16_bundle_lacp.yml       | 16       | interfaces, bundles       | 
| 99_write_report.yml      | 17       | report                    | 