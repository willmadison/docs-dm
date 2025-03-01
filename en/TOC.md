# TiDB Data Migration (DM) Documentation

<!-- markdownlint-disable MD007 -->
<!-- markdownlint-disable MD032 -->

## TOC

+ About DM
  + [What is DM?](overview.md)
  + Basic Features
    - [Table Routing](key-features.md#table-routing)
    - [Block and Allow Lists](key-features.md#block-and-allow-table-lists)
    - [Binlog Event Filter](key-features.md#binlog-event-filter)
  + Advanced Features
    + Merge and Migrate Data from Sharded Tables
      - [Overview](feature-shard-merge.md)
      - [Pessimistic Mode](feature-shard-merge-pessimistic.md)
      - [Optimistic Mode](feature-shard-merge-optimistic.md)
    - [Migrate from MySQL Databases that Use GH-ost/PT-osc](feature-online-ddl.md)
    - [Filter Certain Row Changes Using SQL Expressions](feature-expression-filter.md)
  + [DM Architecture](dm-arch.md)
  + [Benchmarks](benchmark-v2.0-ga.md)
+ Quick Start
  - [Quick Start](quick-start-with-dm.md)
  - [Deploy a DM cluster Using TiUP](deploy-a-dm-cluster-using-tiup.md)
  - [Create a Data Source](quick-start-create-source.md)
  + [Create a Data Migration Task](quick-create-migration-task.md)
     - [Migrate Data from Multiple Data Sources to TiDB](usage-scenario-simple-migration.md)
     - [Migrate Sharded Schemas and Tables to TiDB](usage-scenario-shard-merge.md)
     - [Migrate Incremental Data to TiDB](usage-scenario-incremental-migration.md)
     - [Migrate Tables when There Are More Columns](usage-scenario-downstream-more-columns.md)
+ Deploy
  + [Software and Hardware Requirements](hardware-and-software-requirements.md)
  + Deploy a DM Cluster
    - [Use TiUP (Recommended)](deploy-a-dm-cluster-using-tiup.md)
    - [Use TiUP Offline](deploy-a-dm-cluster-using-tiup-offline.md)
    - [Use Binary](deploy-a-dm-cluster-using-binary.md)
    - [Use Kubernetes (Experimental)](https://docs.pingcap.com/tidb-in-kubernetes/dev/deploy-tidb-dm)
  - [Migrate Data Using DM](migrate-data-using-dm.md)
  - [Test DM Performance](performance-test.md)
+ Maintain
  + Tools
    - [Maintain DM Clusters Using TiUP (Recommended)](maintain-dm-using-tiup.md)
    - [Maintain DM Clusters Using dmctl](dmctl-introduction.md)
  + Cluster Upgrade
    - [Manually Upgrade from v1.0.x to v2.0.x](manually-upgrade-dm-1.0-to-2.0.md)
    - [Upgrade Between v1.0.x](upgrade-dm-1.0.md)
  + [Manage Data Source](manage-source.md)
  + Manage a Data Migration Task
    - [Task Configuration Guide](task-configuration-guide.md)
    - [Precheck a Task](precheck.md)
    - [Create a Task](create-task.md)
    - [Query Status](query-status.md)
    - [Pause a Task](pause-task.md)
    - [Resume a Task](resume-task.md)
    - [Stop a Task](stop-task.md)
    - [Export and Import Data Sources and Task Configuration of Clusters](export-import-config.md)
    - [Handle Failed DDL Statements](handle-failed-ddl-statements.md)
  - [Manually Handle Sharding DDL Lock](manually-handling-sharding-ddl-locks.md)
  - [Manage Schemas of Tables to be Migrated](manage-schema.md)
  - [Handle Alerts](handle-alerts.md)
  - [Daily Check](daily-check.md)
+ Usage Scenarios
  - [Migrate from Aurora to TiDB](migrate-from-mysql-aurora.md)
  - [Migrate when TiDB Tables Have More Columns](usage-scenario-downstream-more-columns.md)
  - [Switch the MySQL Instance to Be Migrated](usage-scenario-master-slave-switch.md)
+ Troubleshoot
  - [Handle Errors](error-handling.md)
  - [Handle Performance Issues](handle-performance-issues.md)
+ Performance Tuning
  - [Optimize Configuration](tune-configuration.md)
+ Reference
  + Architecture
    - [DM Architecture Overview](overview.md)
    - [DM-worker](dm-worker-intro.md)
  - [Command-line Flags](command-line-flags.md)
  + Configuration
    - [Overview](config-overview.md)
    - [DM-master Configuration](dm-master-configuration-file.md)
    - [DM-worker Configuration](dm-worker-configuration-file.md)
    - [Upstream Database Configuration](source-configuration-file.md)
    - [Data Migration Task Configuration](task-configuration-guide.md)
+ Secure
    - [Enable TLS for DM Connections](enable-tls.md)
    - [Generate Self-signed Certificates](generate-self-signed-certificates.md)
  - [Monitoring Metrics](monitor-a-dm-cluster.md)
  - [Alert Rules](alert-rules.md)
  - [Error Codes](error-handling.md#handle-common-errors)
+ [FAQ](faq.md)
+ [Glossary](glossary.md)
+ Release Notes
  + v2.0
    - [2.0.7](releases/2.0.7.md)
    - [2.0.6](releases/2.0.6.md)
    - [2.0.5](releases/2.0.5.md)
    - [2.0.4](releases/2.0.4.md)
    - [2.0.3](releases/2.0.3.md)
    - [2.0.2](releases/2.0.2.md)
    - [2.0.1](releases/2.0.1.md)
    - [2.0 GA](releases/2.0.0-ga.md)
    - [2.0.0-rc.2](releases/2.0.0-rc.2.md)
    - [2.0.0-rc](releases/2.0.0-rc.md)
  + v1.0
    - [1.0.7](releases/1.0.7.md)
    - [1.0.6](releases/1.0.6.md)
    - [1.0.5](releases/1.0.5.md)
    - [1.0.4](releases/1.0.4.md)
    - [1.0.3](releases/1.0.3.md)
    - [1.0.2](releases/1.0.2.md)
