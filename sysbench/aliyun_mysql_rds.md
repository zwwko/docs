# RDS-MySQL基准测试报告 - v1.0.0

## 测试目的
测试RDS-MySQL数据库事务吞吐量。

## 测试环境
### 硬件环境
| 机器       |  OS       |CPU|RAM|
| :-- | :-- | :-- | :--: |
| 云主机A(RDS)| | | |
| 云主机B | CentOS 7.3 64Bit|16核 , Intel(R) Xeon(R) CPU E5-2680 v4 @ 2.40GHz|64GB|
### 软件环境
>*Sysbench 版本: 1.1.0*  
*MySQL版本：5.7.21-log MySQL Community Server (GPL)*  
## RDS-MySQL事务数测试结果：
|序号|线程数|  主机A(RDS-MySQL)事务数(秒) | 云主机B(MySQL)事务数(秒)|
|:--:|:---| :---------: |---------: |
|1| 1  |55.96|204.03|
|2| 64 |3376.83|4221.69|
|3| 128 |4211.13|4204.59|
|4| 500 |5047.11|3262.40|
|5| 1000 |2418.32|2106.66|
|6| 2000 |4643.47|1032.56|

简单分析：
- 云主机A(RDS)单线程时事务数不如云主机B。
- 云主机A(RDS)在线程数1000时，事务数下降比较严重。
- 随着线程数的增加，云主机A(RDS)事务处理能力更具优势。

## 测试详细过程
* 主机A(RDS-MySQL)
```
[root@localhost ~]# sysbench --threads=1 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=10.254.12.95  --mysql-user=wpc --mysql-password=hesc2019_wpc --mysql-db=wpc-ee run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 1
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            7840
        write:                           2240
        other:                           1120
        total:                           11200
    transactions:                        560    (55.96 per sec.)
    queries:                             11200  (1119.20 per sec.)
    ignored errors:                      0      (0.00 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      55.9601
    time elapsed:                        10.0071s
    total number of events:              560
Latency (ms):
         min:                                   11.92
         avg:                                   17.86
         max:                                   45.65
         95th percentile:                       18.61
         sum:                                10004.36
Threads fairness:
    events (avg/stddev):           560.0000/0.00
    execution time (avg/stddev):   10.0044/0.00

[root@localhost ~]# sysbench --threads=64 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=10.254.12.95  --mysql-user=wpc --mysql-password=hesc2019_wpc --mysql-db=wpc-ee run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 64
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            474068
        write:                           135448
        other:                           67724
        total:                           677240
    transactions:                        33862  (3376.83 per sec.)
    queries:                             677240 (67536.66 per sec.)
    ignored errors:                      0      (0.00 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      3376.8332
    time elapsed:                        10.0277s
    total number of events:              33862
Latency (ms):
         min:                                   12.01
         avg:                                   18.91
         max:                                   57.72
         95th percentile:                       26.68
         sum:                               640380.00
Threads fairness:
    events (avg/stddev):           529.0938/28.51
    execution time (avg/stddev):   10.0059/0.01

[root@localhost ~]# sysbench --threads=128 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=10.254.12.95  --mysql-user=wpc --mysql-password=hesc2019_wpc --mysql-db=wpc-ee run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 128
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            592914
        write:                           169404
        other:                           84702
        total:                           847020
    transactions:                        42351  (4211.13 per sec.)
    queries:                             847020 (84222.54 per sec.)
    ignored errors:                      0      (0.00 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      4211.1268
    time elapsed:                        10.0569s
    total number of events:              42351
Latency (ms):
         min:                                   12.31
         avg:                                   30.30
         max:                                   97.42
         95th percentile:                       45.79
         sum:                              1283175.69
Threads fairness:
    events (avg/stddev):           330.8672/46.92
    execution time (avg/stddev):   10.0248/0.02

[root@localhost ~]# sysbench --threads=500 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=10.254.12.95  --mysql-user=wpc --mysql-password=hesc2019_wpc --mysql-db=wpc-ee run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 500
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            716450
        write:                           204697
        other:                           102349
        total:                           1023496
    transactions:                        51174  (5047.11 per sec.)
    queries:                             1023496 (100943.87 per sec.)
    ignored errors:                      1      (0.10 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      5047.1146
    time elapsed:                        10.1393s
    total number of events:              51174
Latency (ms):
         min:                                   12.60
         avg:                                   98.21
         max:                                  454.84
         95th percentile:                      200.47
         sum:                              5025880.58
Threads fairness:
    events (avg/stddev):           102.3480/8.53
    execution time (avg/stddev):   10.0518/0.03

[root@localhost ~]# sysbench --threads=300 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=10.254.12.95  --mysql-user=wpc --mysql-password=hesc2019_wpc --mysql-db=wpc-ee run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 300
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            729946
        write:                           208556
        other:                           104278
        total:                           1042780
    transactions:                        52139  (5169.92 per sec.)
    queries:                             1042780 (103398.36 per sec.)
    ignored errors:                      0      (0.00 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      5169.9182
    time elapsed:                        10.0851s
    total number of events:              52139
Latency (ms):
         min:                                   13.82
         avg:                                   57.69
         max:                                  153.91
         95th percentile:                       94.10
         sum:                              3007894.92
Threads fairness:
    events (avg/stddev):           173.7967/6.32
    execution time (avg/stddev):   10.0263/0.02

[root@localhost ~]# sysbench --threads=1000 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=10.254.12.95  --mysql-user=wpc --mysql-password=hesc2019_wpc --mysql-db=wpc-ee run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 1000
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            361858
        write:                           101541
        other:                           50967
        total:                           514366
    transactions:                        25120  (2418.32 per sec.)
    queries:                             514366 (49518.42 per sec.)
    ignored errors:                      727    (69.99 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      2418.3222
    time elapsed:                        10.3874s
    total number of events:              25120
Latency (ms):
         min:                                   12.71
         avg:                                  406.19
         max:                                 4135.18
         95th percentile:                     1304.21
         sum:                             10203614.88
Threads fairness:
    events (avg/stddev):           25.1200/4.91
    execution time (avg/stddev):   10.2036/0.10

[root@localhost ~]# sysbench --threads=2000 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=10.254.12.95  --mysql-user=wpc --mysql-password=hesc2019_wpc --mysql-db=wpc-ee run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 2000
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            687624
        write:                           196462
        other:                           98231
        total:                           982317
    transactions:                        49115  (4643.47 per sec.)
    queries:                             982317 (92870.96 per sec.)
    ignored errors:                      1      (0.09 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      4643.4677
    time elapsed:                        10.5772s
    total number of events:              49115
Latency (ms):
         min:                                   14.26
         avg:                                  415.98
         max:                                 2807.79
         95th percentile:                     1050.76
         sum:                             20430881.10
Threads fairness:
    events (avg/stddev):           24.5575/4.10
    execution time (avg/stddev):   10.2154/0.16
```
### 云主机B
```shell 
[root@localhost ~]# sysbench --threads=1 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=127.0.0.1 --mysql-user=root --mysql-password=123456 --mysql-db=test_wjl run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 1
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            28574
        write:                           8164
        other:                           4082
        total:                           40820
    transactions:                        2041   (204.03 per sec.)
    queries:                             40820  (4080.51 per sec.)
    ignored errors:                      0      (0.00 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      204.0253
    time elapsed:                        10.0037s
    total number of events:              2041
Latency (ms):
         min:                                    4.05
         avg:                                    4.90
         max:                                   38.31
         95th percentile:                        5.99
         sum:                                 9997.74
Threads fairness:
    events (avg/stddev):           2041.0000/0.00
    execution time (avg/stddev):   9.9977/0.00

[root@localhost ~]# sysbench --threads=64 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=127.0.0.1 --mysql-user=root --mysql-password=123456 --mysql-db=test_wjl run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 64
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            592550
        write:                           169109
        other:                           84586
        total:                           846245
    transactions:                        42261  (4221.69 per sec.)
    queries:                             846245 (84536.11 per sec.)
    ignored errors:                      64     (6.39 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      4221.6859
    time elapsed:                        10.0105s
    total number of events:              42261
Latency (ms):
         min:                                    4.65
         avg:                                   15.14
         max:                                   69.29
         95th percentile:                       24.38
         sum:                               639695.26
Threads fairness:
    events (avg/stddev):           660.3281/8.02
    execution time (avg/stddev):   9.9952/0.00

[root@localhost ~]# sysbench --threads=128 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=127.0.0.1 --mysql-user=root --mysql-password=123456 --mysql-db=test_wjl run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 128
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            592746
        write:                           168788
        other:                           84477
        total:                           846011
    transactions:                        42138  (4204.59 per sec.)
    queries:                             846011 (84416.24 per sec.)
    ignored errors:                      201    (20.06 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      4204.5927
    time elapsed:                        10.0219s
    total number of events:              42138
Latency (ms):
         min:                                    4.89
         avg:                                   30.36
         max:                                  152.02
         95th percentile:                       56.84
         sum:                              1279415.05
Threads fairness:
    events (avg/stddev):           329.2031/7.32
    execution time (avg/stddev):   9.9954/0.01


[root@localhost ~]# sysbench --threads=500 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=127.0.0.1 --mysql-user=root --mysql-password=123456 --mysql-db=test_wjl run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 500
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            500976
        write:                           135184
        other:                           68933
        total:                           705093
    transactions:                        33149  (3262.40 per sec.)
    queries:                             705093 (69392.56 per sec.)
    ignored errors:                      2635   (259.33 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      3262.3980
    time elapsed:                        10.1609s
    total number of events:              33149
Latency (ms):
         min:                                    5.17
         avg:                                  151.51
         max:                                 1401.43
         95th percentile:                      404.61
         sum:                              5022400.64
Threads fairness:
    events (avg/stddev):           66.2980/5.79
    execution time (avg/stddev):   10.0448/0.04

[root@localhost ~]# sysbench --threads=1000 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=127.0.0.1 --mysql-user=root --mysql-password=123456 --mysql-db=test_wjl run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 1000
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            408240
        write:                           94340
        other:                           50969
        total:                           553549
    transactions:                        21809  (2106.66 per sec.)
    queries:                             553549 (53470.58 per sec.)
    ignored errors:                      7351   (710.08 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      2106.6607
    time elapsed:                        10.3524s
    total number of events:              21809
Latency (ms):
         min:                                    5.55
         avg:                                  466.39
         max:                                 5453.97
         95th percentile:                     1506.29
         sum:                             10171418.51
Threads fairness:
    events (avg/stddev):           21.8090/5.04
    execution time (avg/stddev):   10.1714/0.09

[root@localhost ~]# sysbench --threads=1000 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=127.0.0.1 --mysql-user=root --mysql-password=123456 --mysql-db=test_wjl run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 1000
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            397264
        write:                           90930
        other:                           49334
        total:                           537528
    transactions:                        20958  (2023.67 per sec.)
    queries:                             537528 (51902.82 per sec.)
    ignored errors:                      7418   (716.27 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      2023.6699
    time elapsed:                        10.3564s
    total number of events:              20958
Latency (ms):
         min:                                    5.81
         avg:                                  484.88
         max:                                 4037.97
         95th percentile:                     1561.52
         sum:                             10162208.71
Threads fairness:
    events (avg/stddev):           20.9580/5.11
    execution time (avg/stddev):   10.1622/0.10

[root@localhost ~]# sysbench --threads=2000 /usr/local/share/sysbench/oltp_read_write.lua --table-size=200000 --db-driver=mysql --mysql-host=127.0.0.1 --mysql-user=root --mysql-password=123456 --mysql-db=test_wjl run
sysbench 1.1.0 (using bundled LuaJIT 2.1.0-beta3)
Running the test with following options:
Number of threads: 2000
Initializing random number generator from current time
Initializing worker threads...
Threads started!
SQL statistics:
    queries performed:
        read:                            269122
        write:                           53537
        other:                           30773
        total:                           353432
    transactions:                        11550  (1032.56 per sec.)
    queries:                             353432 (31596.45 per sec.)
    ignored errors:                      7673   (685.96 per sec.)
    reconnects:                          0      (0.00 per sec.)
Throughput:
    events/s (eps):                      1032.5580
    time elapsed:                        11.1858s
    total number of events:              11550
Latency (ms):
         min:                                    6.87
         avg:                                 1847.78
         max:                                10990.83
         95th percentile:                     5312.73
         sum:                             21341815.70
Threads fairness:
    events (avg/stddev):           5.7750/2.06
    execution time (avg/stddev):   10.6709/0.32
``` 