
```
sudo -u hdfs hadoop fs -mkdir -p /vlin3
sudo -u hdfs hadoop fs -mkdir -p /jasoncheng22

sudo -u hdfs hadoop jar /opt/cloudera/parcels/CDH-5.9.2-1.cdh5.9.2.p0.3/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen 5000000 /vlin3/input500MB
```

```
[root@ip-172-31-34-74 ~]# sudo -u hdfs hadoop distcp hdfs://ec2-34-210-93-122.us-west-2.compute.amazonaws.com/jasoncheng22/ /
17/05/09 16:49:19 INFO tools.DistCp: Input Options: DistCpOptions{atomicCommit=false, syncFolder=false, deleteMissing=false, ignoreFailures=false, overwrite=false, append=false, useDiff=false, useRdiff=false, fromSnapshot=null, toSnapshot=null, skipCRC=false, blocking=true, numListstatusThreads=0, maxMaps=20, mapBandwidth=100, sslConfigurationFile='null', copyStrategy='uniformsize', preserveStatus=[], preserveRawXattrs=false, atomicWorkPath=null, logPath=null, sourceFileListing=null, sourcePaths=[hdfs://ec2-34-210-93-122.us-west-2.compute.amazonaws.com/jasoncheng22], targetPath=/, targetPathExists=true, filtersFile='null'}
17/05/09 16:49:19 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-34-74.us-west-2.compute.internal/172.31.34.74:8032
17/05/09 16:49:19 INFO tools.SimpleCopyListing: Paths (files+dirs) cnt = 5; dirCnt = 2
17/05/09 16:49:19 INFO tools.SimpleCopyListing: Build file listing completed.
17/05/09 16:49:19 INFO Configuration.deprecation: io.sort.mb is deprecated. Instead, use mapreduce.task.io.sort.mb
17/05/09 16:49:19 INFO Configuration.deprecation: io.sort.factor is deprecated. Instead, use mapreduce.task.io.sort.factor
17/05/09 16:49:19 INFO tools.DistCp: Number of paths in the copy list: 5
17/05/09 16:49:19 INFO tools.DistCp: Number of paths in the copy list: 5
17/05/09 16:49:19 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-34-74.us-west-2.compute.internal/172.31.34.74:8032
17/05/09 16:49:20 INFO mapreduce.JobSubmitter: number of splits:3
17/05/09 16:49:20 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494321531319_0001
17/05/09 16:49:21 INFO impl.YarnClientImpl: Submitted application application_1494321531319_0001
17/05/09 16:49:21 INFO mapreduce.Job: The url to track the job: http://ip-172-31-34-74.us-west-2.compute.internal:8088/proxy/application_1494321531319_0001/
17/05/09 16:49:21 INFO tools.DistCp: DistCp job-id: job_1494321531319_0001
17/05/09 16:49:21 INFO mapreduce.Job: Running job: job_1494321531319_0001
17/05/09 16:49:28 INFO mapreduce.Job: Job job_1494321531319_0001 running in uber mode : false
17/05/09 16:49:28 INFO mapreduce.Job:  map 0% reduce 0%
17/05/09 16:49:38 INFO mapreduce.Job:  map 33% reduce 0%
17/05/09 16:49:40 INFO mapreduce.Job:  map 67% reduce 0%
17/05/09 16:49:41 INFO mapreduce.Job:  map 100% reduce 0%
17/05/09 16:49:41 INFO mapreduce.Job: Job job_1494321531319_0001 completed successfully
17/05/09 16:49:41 INFO mapreduce.Job: Counters: 33
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=385686
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=500002125
                HDFS: Number of bytes written=500000000
                HDFS: Number of read operations=59
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=14
        Job Counters
                Launched map tasks=3
                Other local map tasks=3
                Total time spent by all maps in occupied slots (ms)=26356
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=26356
                Total vcore-seconds taken by all map tasks=26356
                Total megabyte-seconds taken by all map tasks=26988544
        Map-Reduce Framework
                Map input records=5
                Map output records=0
                Input split bytes=348
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=226
                CPU time spent (ms)=12950
                Physical memory (bytes) snapshot=687194112
                Virtual memory (bytes) snapshot=4701421568
                Total committed heap usage (bytes)=1082130432
        File Input Format Counters
                Bytes Read=1777
        File Output Format Counters
                Bytes Written=0
        org.apache.hadoop.tools.mapred.CopyMapper$Counter
                BYTESCOPIED=500000000
                BYTESEXPECTED=500000000
                COPY=5
```


```
 [root@ip-172-31-34-74 ~]# hdfs fsck /vlin3 -files -blocks
Connecting to namenode via http://ip-172-31-34-74.us-west-2.compute.internal:50070
FSCK started by root (auth:SIMPLE) from /172.31.34.74 for path /vlin3 at Tue May 09 16:52:25 UTC 2017
/vlin3 <dir>
/vlin3/input100MB <dir>
/vlin3/input100MB/_SUCCESS 0 bytes, 0 block(s):  OK

/vlin3/input100MB/part-m-00000 50000000 bytes, 1 block(s):  OK
0. BP-1883603607-172.31.34.74-1494264057261:blk_1073742975_2156 len=50000000 Live_repl=3

/vlin3/input100MB/part-m-00001 50000000 bytes, 1 block(s):  OK
0. BP-1883603607-172.31.34.74-1494264057261:blk_1073742976_2157 len=50000000 Live_repl=3

/vlin3/input500MB <dir>
/vlin3/input500MB/_SUCCESS 0 bytes, 0 block(s):  OK

/vlin3/input500MB/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-1883603607-172.31.34.74-1494264057261:blk_1073742952_2133 len=134217728 Live_repl=3
1. BP-1883603607-172.31.34.74-1494264057261:blk_1073742953_2134 len=115782272 Live_repl=3

/vlin3/input500MB/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-1883603607-172.31.34.74-1494264057261:blk_1073742951_2132 len=134217728 Live_repl=3
1. BP-1883603607-172.31.34.74-1494264057261:blk_1073742954_2135 len=115782272 Live_repl=3

Status: HEALTHY
 Total size:    600000000 B
 Total dirs:    3
 Total files:   6
 Total symlinks:                0
 Total blocks (validated):      6 (avg. block size 100000000 B)
 Minimally replicated blocks:   6 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Tue May 09 16:52:25 UTC 2017 in 3 milliseconds


The filesystem under path '/vlin3' is HEALTHY
```

```
[root@ip-172-31-34-74 ~]# hdfs fsck /jasoncheng22 -files -blocks
Connecting to namenode via http://ip-172-31-34-74.us-west-2.compute.internal:50070
FSCK started by root (auth:SIMPLE) from /172.31.34.74 for path /jasoncheng22 at Tue May 09 16:52:46 UTC 2017
/jasoncheng22 <dir>
/jasoncheng22/input500MB <dir>
/jasoncheng22/input500MB/_SUCCESS 0 bytes, 0 block(s):  OK

/jasoncheng22/input500MB/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-1883603607-172.31.34.74-1494264057261:blk_1073743787_2968 len=134217728 Live_repl=3
1. BP-1883603607-172.31.34.74-1494264057261:blk_1073743790_2971 len=115782272 Live_repl=3

/jasoncheng22/input500MB/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-1883603607-172.31.34.74-1494264057261:blk_1073743786_2967 len=134217728 Live_repl=3
1. BP-1883603607-172.31.34.74-1494264057261:blk_1073743789_2970 len=115782272 Live_repl=3

Status: HEALTHY
 Total size:    500000000 B
 Total dirs:    2
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 125000000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Tue May 09 16:52:46 UTC 2017 in 2 milliseconds


The filesystem under path '/jasoncheng22' is HEALTHY
[root@ip-172-31-34-74 ~]#
```