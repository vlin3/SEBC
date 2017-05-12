
##    The full teragen command and job output
```
[root@ip-172-31-25-239 zhou]# su zhou
[zhou@ip-172-31-25-239 zhou]$ time hadoop jar /opt/cloudera/parcels/CDH-5.9.2-1.cdh5.9.2.p0.3/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.map.memory.mb=1024 -Dmapred.map.tasks=6 -Ddfs.block.size=67108864 65536000 /user/zhou/tgen
17/05/12 04:18:59 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-16-149.us-west-2.compute.internal/172.31.16.149:8032
17/05/12 04:19:00 INFO terasort.TeraSort: Generating 65536000 using 6
17/05/12 04:19:00 INFO mapreduce.JobSubmitter: number of splits:6
17/05/12 04:19:00 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/05/12 04:19:00 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/05/12 04:19:00 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494560840895_0003
17/05/12 04:19:00 INFO impl.YarnClientImpl: Submitted application application_1494560840895_0003
17/05/12 04:19:00 INFO mapreduce.Job: The url to track the job: http://ip-172-31-16-149.us-west-2.compute.internal:8088/proxy/application_1494560840895_0003/
17/05/12 04:19:00 INFO mapreduce.Job: Running job: job_1494560840895_0003
17/05/12 04:19:07 INFO mapreduce.Job: Job job_1494560840895_0003 running in uber mode : false
17/05/12 04:19:07 INFO mapreduce.Job:  map 0% reduce 0%
17/05/12 04:19:19 INFO mapreduce.Job:  map 6% reduce 0%
17/05/12 04:19:21 INFO mapreduce.Job:  map 8% reduce 0%
17/05/12 04:19:22 INFO mapreduce.Job:  map 20% reduce 0%
17/05/12 04:19:24 INFO mapreduce.Job:  map 21% reduce 0%
17/05/12 04:19:25 INFO mapreduce.Job:  map 27% reduce 0%
17/05/12 04:19:28 INFO mapreduce.Job:  map 33% reduce 0%
17/05/12 04:19:31 INFO mapreduce.Job:  map 39% reduce 0%
17/05/12 04:19:34 INFO mapreduce.Job:  map 45% reduce 0%
17/05/12 04:19:37 INFO mapreduce.Job:  map 50% reduce 0%
17/05/12 04:19:40 INFO mapreduce.Job:  map 54% reduce 0%
17/05/12 04:19:43 INFO mapreduce.Job:  map 58% reduce 0%
17/05/12 04:19:46 INFO mapreduce.Job:  map 61% reduce 0%
17/05/12 04:19:49 INFO mapreduce.Job:  map 64% reduce 0%
17/05/12 04:19:52 INFO mapreduce.Job:  map 67% reduce 0%
17/05/12 04:19:55 INFO mapreduce.Job:  map 70% reduce 0%
17/05/12 04:19:58 INFO mapreduce.Job:  map 73% reduce 0%
17/05/12 04:20:01 INFO mapreduce.Job:  map 75% reduce 0%
17/05/12 04:20:04 INFO mapreduce.Job:  map 78% reduce 0%
17/05/12 04:20:07 INFO mapreduce.Job:  map 81% reduce 0%
17/05/12 04:20:10 INFO mapreduce.Job:  map 84% reduce 0%
17/05/12 04:20:13 INFO mapreduce.Job:  map 86% reduce 0%
17/05/12 04:20:14 INFO mapreduce.Job:  map 87% reduce 0%
17/05/12 04:20:16 INFO mapreduce.Job:  map 89% reduce 0%
17/05/12 04:20:17 INFO mapreduce.Job:  map 90% reduce 0%
17/05/12 04:20:19 INFO mapreduce.Job:  map 92% reduce 0%
17/05/12 04:20:22 INFO mapreduce.Job:  map 95% reduce 0%
17/05/12 04:20:25 INFO mapreduce.Job:  map 97% reduce 0%
17/05/12 04:20:26 INFO mapreduce.Job:  map 98% reduce 0%
17/05/12 04:20:27 INFO mapreduce.Job:  map 99% reduce 0%
17/05/12 04:20:28 INFO mapreduce.Job:  map 100% reduce 0%
17/05/12 04:20:28 INFO mapreduce.Job: Job job_1494560840895_0003 completed successfully
17/05/12 04:20:28 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=741174
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=511
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=24
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=6
                Other local map tasks=6
                Total time spent by all maps in occupied slots (ms)=421707
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=421707
                Total vcore-seconds taken by all map tasks=421707
                Total megabyte-seconds taken by all map tasks=431827968
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=511
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1201
                CPU time spent (ms)=118560
                Physical memory (bytes) snapshot=1751306240
                Virtual memory (bytes) snapshot=9507389440
                Total committed heap usage (bytes)=2970091520
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000


```

##    The result of the time command
```
real    1m31.555s
user    0m5.056s
sys     0m0.716s

```

##    The command and output of hdfs dfs -ls /user/zhou/tgen
```
[zhou@ip-172-31-25-239 zhou]$ hdfs dfs -ls /user/zhou/tgen
Found 7 items
-rw-r--r--   3 zhou zhou          0 2017-05-12 04:20 /user/zhou/tgen/_SUCCESS
-rw-r--r--   3 zhou zhou 1092266700 2017-05-12 04:20 /user/zhou/tgen/part-m-00000
-rw-r--r--   3 zhou zhou 1092266700 2017-05-12 04:20 /user/zhou/tgen/part-m-00001
-rw-r--r--   3 zhou zhou 1092266600 2017-05-12 04:20 /user/zhou/tgen/part-m-00002
-rw-r--r--   3 zhou zhou 1092266700 2017-05-12 04:20 /user/zhou/tgen/part-m-00003
-rw-r--r--   3 zhou zhou 1092266700 2017-05-12 04:20 /user/zhou/tgen/part-m-00004
-rw-r--r--   3 zhou zhou 1092266600 2017-05-12 04:19 /user/zhou/tgen/part-m-00005
```

