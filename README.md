# prometheus-promql
#This is all query that maybe you will need

1.Check memory usage of the Node in presentage
```
sum by (instance)(100* (1 - ((avg_over_time(node_memory_MemFree_bytes[5m]) + avg_over_time(node_memory_Cached_bytes[5m]) + avg_over_time(node_memory_Buffers_bytes[5m])) / avg_over_time(node_memory_MemTotal_bytes[5m]))))
```
