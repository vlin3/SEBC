## The hostname of your database server
```
[root@ip-172-31-26-189 lib]# hostname
ip-172-31-26-189
```

## The command and output for showing the database server version
```
mysql> SELECT @@version;
+------------+
| @@version  |
+------------+
| 5.6.36-log |
+------------+
1 row in set (0.00 sec)
```

## The command and output for listing the databases created above
```
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
9 rows in set (0.01 sec)
```

