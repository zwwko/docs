<!-- ---
title:阿里云服务器 Sysbench 基准测试报告 - v1.0.0
category: benchmark
draft: true
--- -->
# 阿里云服务器 Sysbench 基准测试报告 - v1.0.0

## 测试目的
测试阿里云服务器CPU性能,线程调度器,互斥锁,内存,数据库等性能。

## 测试环境
### 硬件环境
| 机器       |  OS       |CPU|RAM|
| :-- | :-- | :-- | :--: |
| 台式机A  | CentOS 7.3 64Bit|4核i5-4590 3.3GHz|8GB|
| 阿里云主机B | CentOS 7.3 64Bit|16核 , Intel(R) Xeon(R) CPU E5-2680 v4 @ 2.40GHz|64GB|
### 软件环境
>*Sysbench 版本: 1.1.0*  
*MySQL版本：5.7.21-log MySQL Community Server (GPL)*  
## 测试结果：
|序号| 测试项|  台式机A       | 云主机B|
|:--:|:---| :---------: |---------: |
|1| cpu性能       |1|0.985|
|2| 线程调度性能 |1|0.551|
|3| 互斥锁性能 |1|1.376|
|4| 内存性能 |1|0.652|
|5| 数据库性能(OLTP基准测试) |1|0.583|
|6| 磁盘IO |100MB/s|50.6MB/s|

简单分析：
- 云主机B线程调度性能、内存性能不如台式机A。
- 云主机B的OLTP基准事务数也不如台式机A。
- 这个测试结果说明台式机A的单核处理能力，以内存性能更好。
- 云主机B磁盘IO较低，普通PC磁盘都在100MB/s左右。

## 测试详细过程
* 台式机A
```
1、CPU测试
[root@localhost sysbench-0.5]# sysbench --test=cpu --cpu-max-prime=15000 run
sysbench 0.5: multi-threaded system evaluation benchmark
Running the test with following options:
Number of threads: 1
Random number generator seed is 0 and will be ignored
Prime numbers limit: 15000
Initializing worker threads...
Threads started!
General statistics:
total time: 22.2449s
total number of events: 10000
total time taken by event execution: 22.2425s
response time:
min: 2.20ms
avg: 2.22ms
max: 3.15ms
approx. 95 percentile: 2.21ms
Threads fairness:
events (avg/stddev): 10000.0000/0.00
execution time (avg/stddev): 22.2425/0.00

2、线程测试
# sysbench --test=threads --num-threads=64 run
sysbench 0.5: multi-threaded system evaluation benchmark
Running the test with following options:
Number of threads: 64
Random number generator seed is 0 and will be ignored
Threads started!
General statistics:
total time: 1.8928s
total number of events: 10000
total time taken by event execution: 120.6757s
response time:
min: 0.22ms
avg: 12.07ms
max: 108.04ms
approx. 95 percentile: 34.71ms
Threads fairness:
events (avg/stddev): 156.2500/8.66
execution time (avg/stddev): 1.8856/0.00

3、互斥锁(mutex)
# sysbench --test=mutex --num-threads=16 --mutex-num=2048 --mutex-locks=1000000 --mutex
-loops=5000 run
sysbench 0.5: multi-threaded system evaluation benchmark
Running the test with following options:
Number of threads: 16
Random number generator seed is 0 and will be ignored
Threads started!
General statistics:
total time: 4.6258s
total number of events: 16
total time taken by event execution: 73.8042s
response time:
min: 4596.09ms
avg: 4612.76ms
max: 4625.73ms
approx. 95 percentile: 4624.63ms
Threads fairness:
events (avg/stddev): 1.0000/0.00
execution time (avg/stddev): 4.6128/0.01

4、内存测试
# sysbench --test=memory --memory-block-size=8K --memory-total-size=2G --num-threads=16
run
sysbench 0.5: multi-threaded system evaluation benchmark
Running the test with following options:
Number of threads: 16
Random number generator seed is 0 and will be ignored
Threads started!
Operations performed: 262144 (1436157.48 ops/sec)
2048.00 MB transferred (11219.98 MB/sec)
General statistics:
total time: 0.1825s
total number of events: 262144
total time taken by event execution: 1.7439s
response time:
min: 0.00ms
avg: 0.01ms
max: 5.59ms
approx. 95 percentile: 0.02ms
Threads fairness:
events (avg/stddev): 16384.0000/891.16
execution time (avg/stddev): 0.1090/0.00

5、数据库测试OLTP
[root@dbserver sysbench-0.5]# sysbench --test=/root/sysbench-0.5/sysbench/tests/db/oltp.lua --
oltp-table-size=200000 --db-driver=mysql --mysql-socket=/usr/local/mysql3306/data/mysqld.sock
--mysql-user=root --mysql-password=grid --mysql-db=mysql run
sysbench 0.5: multi-threaded system evaluation benchmark
Running the test with following options:
Number of threads: 1
Random number generator seed is 0 and will be ignored
Initializing worker threads...
Threads started!
OLTP test statistics:
queries performed:
read: 140000
write: 40000
other: 20000
total: 200000
transactions: 10000 (587.72 per sec.)
read/write requests: 180000 (10579.01 per sec.)
other operations: 20000 (1175.45 per sec.)
ignored errors: 0 (0.00 per sec.)
reconnects: 0 (0.00 per sec.)
General statistics:
total time: 17.0148s
total number of events: 10000
total time taken by event execution: 17.0109s
response time:
min: 1.44ms
avg: 1.70ms
max: 71.51ms
approx. 95 percentile: 1.65ms
Threads fairness:
events (avg/stddev): 10000.0000/0.00
execution time (avg/stddev): 17.0109/0.00
```
### 云主机B
```shell 
１、CPU性能测试
sysbench --events=10000 --time=60 --cpu-max-prime=15000 cpu run
Running the test with following options:
Number of threads: 1
Initializing random number generator from current time
Prime numbers limit: 15000
Initializing worker threads...
Threads started!
CPU speed:
    events per second:   442.83
Throughput:
    events/s (eps):                      442.8299
    time elapsed:                        22.5820s
    total number of events:              10000
Latency (ms):
         min:                                    2.25
         avg:                                    2.26
         max:                                    3.20
         95th percentile:                        2.26
         sum:                                22574.14
Threads fairness:
    events (avg/stddev):           10000.0000/0.00
    execution time (avg/stddev):   22.5741/0.00

3、线程测试
sysbench --events=10000 --threads=64 threads run
Running the test with following options:
Number of threads: 64
Initializing random number generator from current time
Initializing worker threads...
Threads started!
Throughput:
    events/s (eps):                      2911.9109
    time elapsed:                        3.4342s
    total number of events:              10000
Latency (ms):
         min:                                    0.30
         avg:                                   21.82
         max:                                  231.81
         95th percentile:                      155.80
         sum:                               218208.31
Threads fairness:
    events (avg/stddev):           156.2500/23.17
    execution time (avg/stddev):   3.4095/0.02

3、互斥锁(mutex)
sysbench --threads=16 --mutex-num=2048 --mutex-locks=1000000 --mutex-loops=5000 mutex run
Running the test with following options:
Number of threads: 16
Initializing random number generator from current time
Initializing worker threads...
Threads started!
Throughput:
    events/s (eps):                      4.7606
    time elapsed:                        3.3609s
    total number of events:              16
Latency (ms):
         min:                                 2306.46
         avg:                                 2785.90
         max:                                 3356.01
         95th percentile:                     3151.62
         sum:                                44574.45
Threads fairness:
    events (avg/stddev):           1.0000/0.00
    execution time (avg/stddev):   2.7859/0.30

4、内存测试
sysbench --memory-block-size=8K --memory-total-size=2G --threads=16 memory run
Running the test with following options:
Number of threads: 16
Initializing random number generator from current time
Running memory speed test with the following options:
  block size: 8KiB
  total size: 2048MiB
  operation: write
  scope: global
Initializing worker threads...
Threads started!
Total operations: 262144 (935770.17 per second)
2048.00 MiB transferred (7310.70 MiB/sec)
Throughput:
    events/s (eps):                      935770.1744
    time elapsed:                        0.2801s
    total number of events:              262144
Latency (ms):
         min:                                    0.00
         avg:                                    0.01
         max:                                    9.11
         95th percentile:                        0.02
         sum:                                 3726.24
Threads fairness:
    events (avg/stddev):           16384.0000/0.00
    execution time (avg/stddev):   0.2329/0.01

5、数据库测试OLTP
//生成20万条数据，数据库名：test_wjl，数据库用户：root，密码：123456
sysbench /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-socket=/opt/mysqldata/mysql.sock --mysql-user=root --mysql-password=123456 --mysql-db=test_wjl prepare
//测试读写
sysbench --time=60 --events=10000 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-socket=/opt/mysqldata/mysql.sock --mysql-user=root --mysql-password=123456 --mysql-db=test_wjl run
//清除测试表
sysbench /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-socket=/opt/mysqldata/mysql.sock --mysql-user=root --mysql-password=123456 --mysql-db=test_wjl cleanup
Running the test with following options:
Number of threads: 1
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            140000
        write:                           40000
        other:                           20000
        total:                           200000
    transactions:                        10000  (342.62 per sec.)
    queries:                             200000 (6852.35 per sec.)
    ignored errors:                      0      (0.00 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      342.6177
    time elapsed:                        29.1870s
    total number of events:              10000
Latency (ms):
         min:                                    2.62
         avg:                                    2.92
         max:                                   24.74
         95th percentile:                        3.19
         sum:                                29163.13
Threads fairness:
    events (avg/stddev):           10000.0000/0.00
    execution time (avg/stddev):   29.1631/0.00

6、磁盘IO性能测试
//在当前目录生成128个16M文件
sysbench fileio prepare
//随机读写测试文件
sysbench --events=10000 fileio --file-testRunning the test with following options:
Number of threads: 1
Initializing random number generator from current time
Extra file open flags: (none)
128 files, 16MiB each
2GiB total file size
Block size 16KiB
Number of IO requests: 10000
Read/Write ratio for combined random IO test: 1.50
Periodic FSYNC enabled, calling fsync() each 100 requests.
Calling fsync() at the end of test, Enabled.
Using synchronous I/O mode
Doing random r/w test
Initializing worker threads...
Threads started!
Throughput:
         read:  IOPS=1853.25 28.96 MiB/s (30.36 MB/s)
         write: IOPS=1235.50 19.30 MiB/s (20.24 MB/s)
         fsync: IOPS=4020.99
Latency (ms):
         min:                                  0.00
         avg:                                  0.14
         max:                                 38.80
         95th percentile:                      0.39
         sum:                               1403.22
``` 

### MySQL优化参数配置
```conf
#在瞬时能够接收的链接数。高并发时需要配置，默认80。
back_log = 500

#最大连接数，视服务器性能，一般不超过2000，最高不超过4000
max_connections = 1000

#对于同一主机，如果有超出该参数值个数的中断错误连接，则该主机将被禁止连接。
#如需对该主机进行解禁，执行：FLUSH HOST。
max_connect_errors = 60000

#物理内存的70%-80%左右，不宜过大
innodb_buffer_pool_size = 48G

#设为1当然是最安全的，但性能页是最差的（相对其他两个参数而言，但不是不能接受）。
#如果对数据一致性和完整性要求不高，完全可以设为2，
#如果只最求性能，例如高并发写的日志服务器，设为0来获得更高性能
innodb_flush_log_at_trx_commit = 2

#表的缓存：2*max_connections-5*max_connections，但是不能大于操作系统文件描述符限制。
#当某一连接访问一个表时，MySQL会检查当前已缓存表的数量。
#如果该表已经在缓存中打开，则会直接访问缓存中的表已加快查询速度；如果该表未被缓存，则会将当前的表添加进缓存并进行查询。
#查看：
#> show global status like ‘open%_tables’;
#> Open_tables正在打开的表数量。
#> Opened_tables曾经打开过的表数量。
#> 如果Open_tables的值已经接近table_open_cache的值，且
#Opened_tables还在不断变大，则需要加大table_open_cache
table_open_cache = 4000

#这个选项是设置 redo 日志（重做日志）的大小。redo 日志 是用来确保写入的数据能够快速地写入，并且持久化，还可以用于崩溃恢复。
#配置大可以提高性能，当时会降低崩溃恢复的速度。 MySQL 5.6，可以设置为4G以上
innodb_log_file_size = 4G

#这个设置项用来设置缓存还没有提交的事务的缓冲区的大小。
#默认值(1MB)一般是够用的，但一旦事务之中带有大 blob/text 字段，这个缓冲区会被很快填满，并引起额外的 I/O 负载。
#看看 innodb_log_waits 这个状态变量的值，如果不是 0 的话，需要增加nnodb_log_buffer_size。
innodb_log_buffer_size = 10M

lower_case_table_names = 1
slow_query_log =1
long_query_time=2
slow_query_log_file=/opt/mysqldata/mysql‐slow.log
```