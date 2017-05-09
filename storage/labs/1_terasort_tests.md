```
[root@ip-172-31-34-74 /]# useradd vlin3
[root@ip-172-31-34-74 /]# passwd vlin3
Changing password for user vlin3.
New password:
BAD PASSWORD: it is based on a dictionary word
Retype new password:
passwd: all authentication tokens updated successfully.

```

```
[root@ip-172-31-34-74 ~]# sudo -u hdfs hadoop fs -mkdir -p /user/vlin3
[root@ip-172-31-34-74 ~]# sudo -u hdfs hadoop fs -chown -R vlin3:supergroup /user/vlin3
[root@ip-172-31-34-74 ~]# su vlin3

[vlin3@ip-172-31-34-74 /]$ time hadoop jar /opt/cloudera/parcels/CDH-5.9.2-1.cdh5.9.2.p0.3/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 10000000 /user/vlin3/File10G
17/05/09 07:59:22 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-34-74.us-west-2.compute.internal/172.31.34.74:8032
17/05/09 07:59:23 INFO terasort.TeraSort: Generating 10000000 using 4
17/05/09 07:59:23 INFO mapreduce.JobSubmitter: number of splits:4
17/05/09 07:59:23 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/05/09 07:59:23 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/05/09 07:59:23 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494301175424_0010
17/05/09 07:59:24 INFO impl.YarnClientImpl: Submitted application application_1494301175424_0010
17/05/09 07:59:24 INFO mapreduce.Job: The url to track the job: http://ip-172-31-34-74.us-west-2.compute.internal:8088/proxy/application_1494301175424_0010/
17/05/09 07:59:24 INFO mapreduce.Job: Running job: job_1494301175424_0010
17/05/09 07:59:30 INFO mapreduce.Job: Job job_1494301175424_0010 running in uber mode : false
17/05/09 07:59:30 INFO mapreduce.Job:  map 0% reduce 0%
17/05/09 07:59:40 INFO mapreduce.Job:  map 50% reduce 0%
17/05/09 07:59:43 INFO mapreduce.Job:  map 100% reduce 0%
17/05/09 07:59:44 INFO mapreduce.Job: Job job_1494301175424_0010 completed successfully
17/05/09 07:59:44 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=494064
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=337
                HDFS: Number of bytes written=1000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=38233
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=38233
                Total vcore-seconds taken by all map tasks=38233
                Total megabyte-seconds taken by all map tasks=39150592
        Map-Reduce Framework
                Map input records=10000000
                Map output records=10000000
                Input split bytes=337
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=415
                CPU time spent (ms)=30100
                Physical memory (bytes) snapshot=1461755904
                Virtual memory (bytes) snapshot=6257410048
                Total committed heap usage (bytes)=1742209024
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=21472776955442690
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=1000000000

real    0m24.917s
user    0m5.773s
sys     0m0.726s
```

```
[vlin3@ip-172-31-34-74 /]$ time hadoop jar /opt/cloudera/parcels/CDH-5.9.2-1.cdh5.9.2.p0.3/lib/hadoop-0.20-mapreduce/hadoop-examples.jar  terasort /user/vlin3/File10G /user/vlin3/terasort-output
17/05/09 08:12:40 INFO terasort.TeraSort: starting
17/05/09 08:12:41 INFO input.FileInputFormat: Total input paths to process : 4
Spent 174ms computing base-splits.
Spent 3ms computing TeraScheduler splits.
Computing input splits took 178ms
Sampling 10 splits of 32
Making 8 from 100000 sampled records
Computing parititions took 881ms
Spent 1062ms computing partitions.
17/05/09 08:12:42 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-34-74.us-west-2.compute.internal/172.31.34.74:8032
17/05/09 08:12:43 INFO mapreduce.JobSubmitter: number of splits:32
17/05/09 08:12:43 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494301175424_0011
17/05/09 08:12:43 INFO impl.YarnClientImpl: Submitted application application_1494301175424_0011
17/05/09 08:12:43 INFO mapreduce.Job: The url to track the job: http://ip-172-31-34-74.us-west-2.compute.internal:8088/proxy/application_1494301175424_0011/
17/05/09 08:12:43 INFO mapreduce.Job: Running job: job_1494301175424_0011
17/05/09 08:12:51 INFO mapreduce.Job: Job job_1494301175424_0011 running in uber mode : false
17/05/09 08:12:51 INFO mapreduce.Job:  map 0% reduce 0%
17/05/09 08:12:58 INFO mapreduce.Job:  map 3% reduce 0%
17/05/09 08:13:00 INFO mapreduce.Job:  map 22% reduce 0%
17/05/09 08:13:05 INFO mapreduce.Job:  map 25% reduce 0%
17/05/09 08:13:07 INFO mapreduce.Job:  map 28% reduce 0%
17/05/09 08:13:08 INFO mapreduce.Job:  map 41% reduce 0%
17/05/09 08:13:09 INFO mapreduce.Job:  map 44% reduce 0%
17/05/09 08:13:12 INFO mapreduce.Job:  map 47% reduce 0%
17/05/09 08:13:15 INFO mapreduce.Job:  map 50% reduce 0%
17/05/09 08:13:16 INFO mapreduce.Job:  map 53% reduce 0%
17/05/09 08:13:17 INFO mapreduce.Job:  map 66% reduce 0%
17/05/09 08:13:19 INFO mapreduce.Job:  map 69% reduce 0%
17/05/09 08:13:23 INFO mapreduce.Job:  map 72% reduce 0%
17/05/09 08:13:24 INFO mapreduce.Job:  map 81% reduce 0%
17/05/09 08:13:25 INFO mapreduce.Job:  map 88% reduce 0%
17/05/09 08:13:26 INFO mapreduce.Job:  map 91% reduce 0%
17/05/09 08:13:31 INFO mapreduce.Job:  map 97% reduce 0%
17/05/09 08:13:32 INFO mapreduce.Job:  map 100% reduce 0%
17/05/09 08:13:35 INFO mapreduce.Job:  map 100% reduce 13%
17/05/09 08:13:37 INFO mapreduce.Job:  map 100% reduce 25%
17/05/09 08:13:38 INFO mapreduce.Job:  map 100% reduce 50%
17/05/09 08:13:41 INFO mapreduce.Job:  map 100% reduce 75%
17/05/09 08:13:42 INFO mapreduce.Job:  map 100% reduce 88%
17/05/09 08:13:44 INFO mapreduce.Job:  map 100% reduce 100%
17/05/09 08:13:44 INFO mapreduce.Job: Job job_1494301175424_0011 completed successfully
17/05/09 08:13:44 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=443033471
                FILE: Number of bytes written=885300103
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1000004832
                HDFS: Number of bytes written=1000000000
                HDFS: Number of read operations=120
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=32
                Launched reduce tasks=8
                Data-local map tasks=31
                Rack-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=217842
                Total time spent by all reduces in occupied slots (ms)=73296
                Total time spent by all map tasks (ms)=217842
                Total time spent by all reduce tasks (ms)=73296
                Total vcore-seconds taken by all map tasks=217842
                Total vcore-seconds taken by all reduce tasks=73296
                Total megabyte-seconds taken by all map tasks=223070208
                Total megabyte-seconds taken by all reduce tasks=75055104
        Map-Reduce Framework
                Map input records=10000000
                Map output records=10000000
                Map output bytes=1020000000
                Map output materialized bytes=437266258
                Input split bytes=4832
                Combine input records=0
                Combine output records=0
                Reduce input groups=10000000
                Reduce shuffle bytes=437266258
                Reduce input records=10000000
                Reduce output records=10000000
                Spilled Records=20000000
                Shuffled Maps =256
                Failed Shuffles=0
                Merged Map outputs=256
                GC time elapsed (ms)=3688
                CPU time spent (ms)=166510
                Physical memory (bytes) snapshot=18217926656
                Virtual memory (bytes) snapshot=62714519552
                Total committed heap usage (bytes)=21124612096
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=1000000000
        File Output Format Counters
                Bytes Written=1000000000
17/05/09 08:13:44 INFO terasort.TeraSort: done

real    1m5.950s
user    0m7.830s
sys     0m0.845s
```

