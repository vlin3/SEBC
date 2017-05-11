```
[root@ip-172-31-34-74 ~]# beeline
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-34-74.us-west-2.compute.internal:10000/default;principal=hi
scan complete in 4ms
Connecting to jdbc:hive2://ip-172-31-34-74.us-west-2.compute.internal:10000/default;principal=hive/i
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-34-74.us-west-2.com> show tables;
INFO  : Compiling command(queryId=hive_20170511084848_8d2b02fc-29f4-4408-b572-55d4e62b548c): show ta
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:
INFO  : Completed compiling command(queryId=hive_20170511084848_8d2b02fc-29f4-4408-b572-55d4e62b548c
INFO  : Executing command(queryId=hive_20170511084848_8d2b02fc-29f4-4408-b572-55d4e62b548c): show ta
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170511084848_8d2b02fc-29f4-4408-b572-55d4e62b548c
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (0.351 seconds)
0: jdbc:hive2://ip-172-31-34-74.us-west-2.com> Write failed: Broken pipe
[root@staffportalapp victor]#

```



```
[root@ip-172-31-34-74 ~]# kinit george@VLIN3.COM
Password for george@VLIN3.COM:
[root@ip-172-31-34-74 ~]# beeline
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-34-74.us-west-2.compute.internal:10000/default;principal=hive/ip-172-31-34-74.us-west-2.compute.internal@VLIN3.COM
scan complete in 3ms
Connecting to jdbc:hive2://ip-172-31-34-74.us-west-2.compute.internal:10000/default;principal=hive/ip-172-31-34-74.us-west-2.compute.internal@VLIN3.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-34-74.us-west-2.com> show tables;
INFO  : Compiling command(queryId=hive_20170511100404_9d3a6568-5899-424e-bdf3-ba91401ce472): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170511100404_9d3a6568-5899-424e-bdf3-ba91401ce472); Time taken: 0.075 seconds
INFO  : Executing command(queryId=hive_20170511100404_9d3a6568-5899-424e-bdf3-ba91401ce472): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170511100404_9d3a6568-5899-424e-bdf3-ba91401ce472); Time taken: 0.14 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
| sample    |
+-----------+--+
1 row selected (0.39 seconds)
0: jdbc:hive2://ip-172-31-34-74.us-west-2.com>

```


```
[root@ip-172-31-34-74 ~]# kinit ferdinand@VLIN3.COM
Password for ferdinand@VLIN3.COM:
[root@ip-172-31-34-74 ~]# beeline
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-34-74.us-west-2.compute.internal:10000/default;principal=hive/ip-172-31-34-74.us-west-2.compute.internal@VLIN3.COM
scan complete in 2ms
Connecting to jdbc:hive2://ip-172-31-34-74.us-west-2.compute.internal:10000/default;principal=hive/ip-172-31-34-74.us-west-2.compute.internal@VLIN3.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-34-74.us-west-2.com> show tables;
INFO  : Compiling command(queryId=hive_20170511101111_c79c2652-aed4-4abe-b0ef-9d243b16e476): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170511101111_c79c2652-aed4-4abe-b0ef-9d243b16e476); Time taken: 0.055 seconds
INFO  : Executing command(queryId=hive_20170511101111_c79c2652-aed4-4abe-b0ef-9d243b16e476): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170511101111_c79c2652-aed4-4abe-b0ef-9d243b16e476); Time taken: 0.126 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (0.289 seconds)
0: jdbc:hive2://ip-172-31-34-74.us-west-2.com>

```