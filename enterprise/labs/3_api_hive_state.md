## check status
```
[root@ip-172-31-34-74 ~]# curl -u admin:admin 'http://localhost:7180/api/v2/clusters/vlin3/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-34-74.us-west-2.compute.internal:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD"
  } ],
  "configStale" : false,
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive"
}[root@ip-172-31-34-74 ~]# 
```

## stop hive
```
[root@ip-172-31-34-74 ~]# curl -X POST -u admin:admin 'http://localhost:7180/api/v2/clusters/vlin3/services/hive/commands/stop'
{
  "id" : 672,
  "name" : "Stop",
  "startTime" : "2017-05-10T04:24:22.912Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}[root@ip-172-31-34-74 ~]# 
```

## check process
```
[root@ip-172-31-34-74 ~]# curl -X POST -u admin:admin 'http://localhost:7180/api/v2/commands/672'
{
  "id" : 672,
  "name" : "Stop",
  "startTime" : "2017-05-10T04:24:22.912Z",
  "endTime" : "2017-05-10T04:24:27.108Z",
  "active" : false,
  "success" : true,
  "resultMessage" : "Successfully stopped service.",
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  },
  "children" : {
    "items" : [ {
      "id" : 674,
      "name" : "Stop",
      "startTime" : "2017-05-10T04:24:22.916Z",
      "endTime" : "2017-05-10T04:24:27.107Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully stopped process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVESERVER2-a9385a6b69af2022eb6fd16b6db129c4"
      }
    }, {
      "id" : 673,
      "name" : "Stop",
      "startTime" : "2017-05-10T04:24:22.914Z",
      "endTime" : "2017-05-10T04:24:27.093Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully stopped process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVEMETASTORE-a9385a6b69af2022eb6fd16b6db129c4"
      }
    } ]
  }
}[root@ip-172-31-34-74 ~]# 
```

## start hive
```
[root@ip-172-31-34-74 ~]# 
[root@ip-172-31-34-74 ~]# curl -X POST -u admin:admin 'http://localhost:7180/api/v2/clusters/vlin3/services/hive/commands/start'
{
  "id" : 676,
  "name" : "Start",
  "startTime" : "2017-05-10T04:26:38.176Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}[root@ip-172-31-34-74 ~]# 
```

## check process
```
[root@ip-172-31-34-74 ~]# 
[root@ip-172-31-34-74 ~]# curl -u admin:admin 'http://localhost:7180/api/v2/commands/676'
{
  "id" : 676,
  "name" : "Start",
  "startTime" : "2017-05-10T04:26:38.176Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  },
  "children" : {
    "items" : [ {
      "id" : 678,
      "name" : "Start",
      "startTime" : "2017-05-10T04:26:38.355Z",
      "active" : true,
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVESERVER2-a9385a6b69af2022eb6fd16b6db129c4"
      }
    }, {
      "id" : 677,
      "name" : "Start",
      "startTime" : "2017-05-10T04:26:38.228Z",
      "active" : true,
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVEMETASTORE-a9385a6b69af2022eb6fd16b6db129c4"
      }
    } ]
  }
}[root@ip-172-31-34-74 ~]# 
```

## check hive status
```
[root@ip-172-31-34-74 ~]# 
[root@ip-172-31-34-74 ~]# curl -u admin:admin 'http://localhost:7180/api/v2/clusters/vlin3/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-34-74.us-west-2.compute.internal:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD"
  } ],
  "configStale" : false,
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive"
}[root@ip-172-31-34-74 ~]# 
```
