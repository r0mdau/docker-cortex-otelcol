docker cortex otelcol
=====================

Simple docker-compose project to run :
* [prometheus-node-exporter](https://github.com/prometheus/node_exporter)
* [opentelemetry-collector-contrib](https://github.com/open-telemetry/opentelemetry-collector-contrib)
* [cortex](https://github.com/cortexproject/cortex)
* [grafana](https://github.com/grafana/grafana)

Schema :
```
+--------------------+      +---------+      +-------------+
|                    |      |         |      |             |
| node_exporter:9100 |<-----| otelcol |----->| cortex:9009 |<---+
|                    |      |         |      |             |    |
+--------------------+      +---------+      +-------------+    |
                                                                |
                                                                |
                        +-------------+     +--------------+    |
                        |             |     |              |    |
                        | web browser |---->| grafana:3000 |----+
                        |             |     |              |
                        +-------------+     +--------------+
```
