## /etc/yum.repos.d
```
[root@ip-172-31-25-239 schema]# ls /etc/yum.repos.d
CentOS-Base.repo  CentOS-Debuginfo.repo  CentOS-Media.repo  CentOS-Vault.repo  cloudera-manager.repo  mysql-community.repo
[root@ip-172-31-25-239 schema]#
```

## setup schema
```
[root@ip-172-31-25-239 schema]# sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql -h ip-172-31-26-189.us-west-2.compute.internal -utemp -ptemp --scm-host ip-172-31-25-239.us-west-2.compute.internal scm scm scm
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!
[root@ip-172-31-25-239 schema]#
```
