# Dashboard Diagram

```
 data_fetch_daemon <----> switch_exec <------------------------------------ switch configs
       |              '-> switch_exec <------------------------------------ switch bridge address-table
   (file system)      '-> mcollective <- mcollective_agent-network_agent <- mcollective data
       |              '-> snmpwalk    <------------------------------------ switch snmp
 switch_data_parser
       |
     (hash)
       |
  data_translator
       |
    (class)
       |
   data_mapper / test_dash -------> graphty (switch infrastructure)
       |                       '--> graphty (machine infrastructure)
  (database)
```
