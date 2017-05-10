## Report the latest available version of the API
```
[root@ip-172-31-34-74 cloudera-scm-server]# curl -u admin:admin 'http://localhost:7180/api/version'
v15
```

## Report the CM version
```
[root@ip-172-31-34-74 cloudera-scm-server]# curl -u admin:admin 'http://localhost:7180/api/v15/cm/version'
{
  "version" : "5.10.1",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170319-2001",
  "gitHash" : "f226435f6fa5f545543c00245900ae43bea7a29c",
  "snapshot" : false
}
```

## List all CM users
```
[root@ip-172-31-34-74 cloudera-scm-server]# curl -u admin:admin 'http://localhost:7180/api/v15/users'
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
[root@ip-172-31-34-74 cloudera-scm-server]# curl -u admin:admin 'http://localhost:7180/api/v15/cm/scmDbInfo'
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```