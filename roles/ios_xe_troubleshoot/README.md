# Role: ios_xe_health_check

Performs health data collection and alerting across Cisco IOS-XE devices. 

See the top-level README.md for full usage instructions.

## Task Files

| File               | Sections | Tags         |
|--------------------|----------|--------------|
| preflight.yml      | —        | always       |
| system.yml         | 1, 2     | system       |
| platform_health.yml| 3        | health       |
| cpu.yml            | 4        | cpu          |
| memory.yml         | 5        | memory       |
| interfaces.yml     | 6, 7     | interfaces   |
| transceivers.yml   | 8        | transceivers |
| topology.yml       | 9        | topology     |
| ospf.yml           | 10       | ospf         |
| bgp.yml            | 11       | bgp          |
| logs.yml           | 12       | logs         |
| report.yml         | 13       | report       |
