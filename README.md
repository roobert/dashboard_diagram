# Dashboard Diagram

```
 data_fetch_daemon <----> switch_exec <------------------------------------ switch configs
       |              '-> switch_exec <------------------------------------ switch bridge address-table
.->(file system)      '-> mcollective <- mcollective_agent-network_agent <- mcollective data
|      |              '-> snmpwalk    <------------------------------------ switch snmp
|  switch_data_parser
|      |
'--->(hash)
       |
  data_translator
       |
    (class)
       |
   data_mapper / test_dash -------> graphty (switch infrastructure)
       |                       '--> graphty (machine infrastructure)
  (database)
```

# TODO

* switch_exec fails if enable password is supplied but switch doesnt require one..
* http frontend to data_fetch_daemon
* test to see if data_fetch_daemon data is valid data?
* test_dashboard refactor
* potentially remove data_translator..
* data parser for snmp
* add graphty..
* move data loader stuff out of test_dash...

1. fetch data
1. copy data locally
1. parse data
1. translate data
1. map data to database
1. dashboard uses views..
