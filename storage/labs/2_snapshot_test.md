```
[vlin3@ip-172-31-34-74 root]$ hadoop fs -mkdir /user/vlin3/precious
[vlin3@ip-172-31-34-74 root]$ hadoop fs -ls /user/vlin3/precious
Found 1 items
-rw-r--r--   3 vlin3 supergroup     474957 2017-05-09 08:57 /user/vlin3/precious/SEBC-Shanghai.zip
```

```
[vlin3@ip-172-31-34-74 root]$ exit
exit
[root@ip-172-31-34-74 ~]# sudo -u hdfs hadoop dfsadmin -allowSnapshot /user/vlin3/precious
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Allowing snaphot on /user/vlin3/precious succeeded
```

```
[root@ip-172-31-34-74 ~]# su vlin3
[vlin3@ip-172-31-34-74 root]$ hadoop dfs -createSnapshot /user/vlin3/precious sebc-hdfs-test
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Created snapshot /user/vlin3/precious/.snapshot/sebc-hdfs-test
```

```
[vlin3@ip-172-31-34-74 root]$ hadoop fs -rm -R /user/vlin3/precious
rm: Failed to move to trash: hdfs://ip-172-31-34-74.us-west-2.compute.internal:8020/user/vlin3/precious: The directory /user/vlin3/precious cannot be deleted since /user/vlin3/precious is snapshottable and already has snapshots
```

```
[vlin3@ip-172-31-34-74 root]$ hadoop fs -rm /user/vlin3/precious/SEBC-Shanghai.zip
17/05/09 08:59:44 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-34-74.us-west-2.compute.internal:8020/user/vlin3/precious/SEBC-Shanghai.zip' to trash at: hdfs://ip-172-31-34-74.us-west-2.compute.internal:8020/user/vlin3/.Trash/Current/user/vlin3/precious/SEBC-Shanghai.zip1494320384250
```

```
[vlin3@ip-172-31-34-74 root]$ hadoop fs -ls /user/vlin3/precious
[vlin3@ip-172-31-34-74 root]$ hadoop fs -cp /user/vlin3/precious/.snapshot/sebc-hdfs-test/SEBC-Shanghai.zip /user/vlin3/precious/
[vlin3@ip-172-31-34-74 root]$ hadoop fs -ls /user/vlin3/precious
Found 1 items
-rw-r--r--   3 vlin3 supergroup     474957 2017-05-09 09:01 /user/vlin3/precious/SEBC-Shanghai.zip
```