## What is ubertask optimization?
```	
The small-jobs "ubertask" optimization, which runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.	```

## Where in CM is the Kerberos Security Realm value displayed?
```
Administration->Settings->CATEGORY->Kerberos->Kerberos Security Realm 
```

## Which CDH service(s) host a property for enabling Kerberos authentication?
```
Zookeeper,HDFS,YARN,HIVE,Oozie,Hue
```

## How do you upgrade the CM agents?
```
More details - https://www.cloudera.com/documentation/enterprise/5-9-x/topics/cm_ag_ug_cm5.html#concept_gs4_bsg_xw

-Stop all CDH services, then Cloudera Manager Server and Cloudera Manager database
-Stop the Cloudera Manager Agent on the Cloudera Manager host
-Download the latest cloudera-manager.repo file for your distribution
-copy the cloudera-manager.repo file to /etc/yum.repos.d/
-sudo yum clean all
-sudo yum upgrade cloudera-manager-agent
-sudo service cloudera-scm-agent start
-Login to Cloudera Manager console and follow on-screen instructions to update
```

## Give the  tsquery  statement used to chart Hue's CPU utilization?
```
select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=hue
```

## Name all the roles that make up the Hive service
```
Hive Gateway
Hive Metastore Server
HiveServer2
WebHCat Server
```

## What steps must be completed before integrating Cloudera Manager with Kerberos?
```
-working KDC and realm
-secured communication between Cloudera Manager server and all agents
-installed openldap-clients on the Cloudera Manager host
-installed krb5-workstation and krb5-libs packages on all hosts
```