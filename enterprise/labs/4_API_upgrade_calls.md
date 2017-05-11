## Report the latest available version of the API
```
[root@ip-172-31-34-74 cloudera-scm-server]# curl -u admin:admin 'http://localhost:7180/api/version'
v16
```

## Report the CM version
```
[root@ip-172-31-34-74 cloudera-scm-server]# curl -u admin:admin 'http://localhost:7180/api/v16/cm/version'
{
  "version" : "5.11.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170412-1249",
  "gitHash" : "70cb1442626406432a6e7af5bdf206a384ca3f98",
  "snapshot" : false
}
```

## List all CM users
```
[root@ip-172-31-34-74 cloudera-scm-server]# curl -u admin:admin 'http://localhost:7180/api/v16/users'
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  }, {
    "name" : "vlin3",
    "roles" : [ "ROLE_ADMIN" ]
  } ]
}
```

## Report the database server in use by CM
```
[root@ip-172-31-34-74 cloudera-scm-server]# curl -u admin:admin 'http://localhost:7180/api/v16/cm/scmDbInfo'
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```