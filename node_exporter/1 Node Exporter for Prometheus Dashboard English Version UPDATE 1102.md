### Grafana v6.4.2 + node_exporter 0.18.1 test pass

#### The dashboard is quite practical, to optimize the main metrics for display, and supporting Node Exporter v0.16 and above.Includes: CPU,memory,disk I/O, network traffic, temperature and other monitoring metrics.

## Notes:

------
#### After import the dashboard, please click `Dashboardsettings`-- `Variables` to set the variable in the upper right corner of the dashboard according to the actual situation。

**The three variables:`$job`, `$hostname` and `$node` will be set and associated by default. **(`$name`, `$env` variable is a custom label and was hidden. You can increase by yourself if needed.)

- `$node` takes the `instance` of node_exporter, `ip:port` format. Most queries are associated with this variable, please make sure it is valid.

- `$maxmount` is used to check the maximum partition of the current host. Normally can only obtain partitions of type `ext4` and `xfs` by default.
------
### Github：

https://github.com/starsliao/Prometheus

### 【update】：
#### 2019/11/2
1. Adjusted the display metrics and descriptions of the Network Sockstat to make it more practical.
2. Modified the display and description of the `node_disk_io_time_seconds_total` metrics.
3. Add the reference value to the chart for each I/O read/write time-consuming.
4. Optimized the display effect of part graph, fixed the color of some lines.
#### 2019/10/30
1. The pie chart that needs to be manually installed was removed, and the pie chart of the original disk information is integrated into the disk table information.
2. Add a Bar Gauge to timely display the information such as cpu,memory , etc.
3. Add a graph to turn on context switching and opening files.
4. To separate the `Time Spent Doing I/Os` from the cpu usage graph.
5. Most of the charts in the entire dashboard have been adjusted and optimized to enhance the practicality and compatibility.
6. Fixed the issue about report error of displaying multiple server partial charts at the same time.
#### 2019/7/1
1. Add usage graph of disk partitions.
2. Optimized data display effect.
#### 2019/5/20
1. Add server list multi-select support, graphs can display data of multiple servers.
2. Optimized the display effect of variables.
3. Optimize the description of some monitoring metrics, click the "i" in the upper left corner of the chart to view.
#### 2019/1/9
1. Fixed a bug that showed inaccurate memory usage.
2. Add a link to update node_exporter and dashboard.
#### 11/16
1. Add description of the variable.
2. Optimized the display speed after the new installation of the dashboard
#### 11/15
1. Add an environment to group servers.
2. Add the pie chart and total disk space.
3. Add the descriptor about current opened file.
4. Add the description of some monitoring metrics.
5. Optimized the display results of some metrics.
#### 11/13
1. Add the ratio of a graph of disk's I/O operation consuming time per second.