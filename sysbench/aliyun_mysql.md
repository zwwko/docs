---
title:阿里云服务器 Sysbench 基准测试报告 - v1.0.0
category: benchmark
draft: true
---

# 阿里云服务器 Sysbench 基准测试报告 - v1.0.0

## 测试目的

测试阿里云服务器CPU性能,磁盘IO,线程调度器,互斥锁,内存,数据库等性能。

> **注意**: 不同的测试环境可能使测试结果发生改变。

## 测试版本、时间、地点
MySQL 版本：5.7.21-log MySQL Community Server (GPL)   
时间：2019 年 4 月 24 日  
地点：杭州

## 测试环境

阿里云主机

| 类别       |  名称       |
| :--------: | :---------: |
| OS       | CentOS 7.3 64Bit       |
| CPU | 16核 , Intel(R) Xeon(R) CPU E5-2680 v4 @ 2.40GHz |
| RAM | 64GB |
| DISK | 53.7 GB + 1073.7 GB |

Sysbench 版本: 1.1.0

## １、CPU性能测试
### 测试说明
```
通过求得15000以内的最大素数,测试单核cpu计算能力
```

### 测试脚本
```shell 
sysbench --cpu-max-prime=15000 cpu run 
```

### 测试结果
```
Running the test with following options:
Number of threads: 1
Initializing random number generator from current time


Prime numbers limit: 15000

Initializing worker threads...

Threads started!

CPU speed:
    events per second:   442.86

Throughput:
    events/s (eps):                      442.8586
    time elapsed:                        10.0009s
    total number of events:              4429

Latency (ms):
         min:                                    2.25
         avg:                                    2.26
         max:                                    2.49
         95th percentile:                        2.26
         sum:                                 9996.41

Threads fairness:
    events (avg/stddev):           4429.0000/0.00
    execution time (avg/stddev):   9.9964/0.00
```
  **重点看：**
```
Latency avg: 2.26ms(平均执行时间越少越好)
```
## 2、磁盘IO性能测试
### 测试说明
```
通过生成128个64M磁盘文件，然后随机读写，测试磁盘随机读写性能
```
### 测试脚本
```shell 
//在当前目录生成128个16M文件
sysbench fileio prepare
//随机读写测试文件
sysbench fileio --file-test-mode=rndrw run
//清空测试文件
sysbench fileio cleanup
```

### 测试结果

``` 
Running the test with following options:
Number of threads: 1
Initializing random number generator from current time


Extra file open flags: (none)
128 files, 16MiB each
2GiB total file size
Block size 16KiB
Number of IO requests: 0
Read/Write ratio for combined random IO test: 1.50
Periodic FSYNC enabled, calling fsync() each 100 requests.
Calling fsync() at the end of test, Enabled.
Using synchronous I/O mode
Doing random r/w test
Initializing worker threads...

Threads started!


Throughput:
         read:  IOPS=1857.00 29.02 MiB/s (30.43 MB/s)
         write: IOPS=1238.00 19.34 MiB/s (20.28 MB/s)
         fsync: IOPS=3968.59

Latency (ms):
         min:                                  0.00
         avg:                                  0.14
         max:                                 38.67
         95th percentile:                      0.40
         sum:                               9921.26
```
  **重点看：**
```
Throughput read: 29.02 MiB/s
Throughput write: 19.34 MiB/s
```
## 3、线程性能测试
### 测试说明
``` 
测试线程调度器的性能，对于高负载情况下测试线程调度器的行为非常有用
```
### 测试脚本
```shell 
sysbench --threads=64 threads run
```
### 测试结果
``` 
Running the test with following options:
Number of threads: 64
Initializing random number generator from current time


Initializing worker threads...

Threads started!


Throughput:
    events/s (eps):                      3260.2227
    time elapsed:                        10.0775s
    total number of events:              32855

Latency (ms):
         min:                                    0.28
         avg:                                   19.58
         max:                                  219.03
         95th percentile:                      153.02
         sum:                               643441.83

Threads fairness:
    events (avg/stddev):           513.3594/41.76
    execution time (avg/stddev):   10.0538/0.02
``` 
  **重点看：**
```
Throughput events/s (eps): 3260.2227(吞吐量越大越好)
Latency avg: 19.58ms(平均执行时间越少越好)
```


## 4、互斥锁(mutex)
* 测试说明
``` 
测试互斥锁的性能，方式是模拟所有线程在同一时刻并发运行，并都短暂请求互斥锁
```
* 测试脚本
```shell 
sysbench --threads=16 --mutex-num=2048 --mutex-locks=1000000 --mutex-loops=5000 mutex run
```
* 测试结果
``` 
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
``` 
  **重点看：**
```
Latency avg: 19.58ms
Threads fairness execution time  (avg): 2.7859
```
## 5、内存测试
### 测试说明
``` 
测试内存读写速度
```
### 测试脚本
``` 
sysbench --memory-block-size=8K --memory-total-size=2G --threads=16 memory run
```
### 测试结果
``` 
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
``` 
  **重点看：**
```
Total operations: 262144 (935770.17 per second)
2048.00 MiB transferred (7310.70 MiB/sec)
```
## 6、MySQL数据库测试OLTP
### 测试说明
``` 
测试数据库读写性能
```
### 测试脚本
```
//生成20万条数据，数据库名：test_wjl，数据库用户：root，密码：123456
sysbench /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-socket=/opt/mysqldata/mysql.sock --mysql-user=root --mysql-password=123456 --mysql-db=test_wjl prepare
//测试读写
sysbench /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-socket=/opt/mysqldata/mysql.sock --mysql-user=root --mysql-password=123456 --mysql-db=test_wjl run
//清除测试表
sysbench /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-socket=/opt/mysqldata/mysql.sock --mysql-user=root --mysql-password=123456 --mysql-db=test_wjl cleanup

```
### 测试结果
``` 
Running the test with following options:
Number of threads: 1
Initializing random number generator from current time


Initializing worker threads...

Threads started!

SQL statistics:
    queries performed:
        read:                            47292
        write:                           13512
        other:                           6756
        total:                           67560
    transactions:                        3378   (337.78 per sec.)
    queries:                             67560  (6755.56 per sec.)
    ignored errors:                      0      (0.00 per sec.)
    reconnects:                          0      (0.00 per sec.)

Throughput:
    events/s (eps):                      337.7782
    time elapsed:                        10.0006s
    total number of events:              3378

Latency (ms):
         min:                                    2.65
         avg:                                    2.96
         max:                                   26.72
         95th percentile:                        3.25
         sum:                                 9992.44

Threads fairness:
    events (avg/stddev):           3378.0000/0.00
    execution time (avg/stddev):   9.9924/0.00
``` 
  **重点看：**
```
transactions: 3378
```