```
[root@ip-172-31-34-74 ~]# curl -u admin:admin 'http://localhost:7180/api/v2/cm/deployment'
{
  "timestamp" : "2017-05-10T03:38:02.135Z",
  "clusters" : [ {
    "name" : "vlin3",
    "version" : "CDH5",
    "services" : [ {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-34-74.us-west-2.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "password"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "root"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "362807296"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "spark_on_yarn_service",
          "value" : "spark_on_yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2cxapghs3aorc8p6zg1or33eq"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "ks_indexer",
      "type" : "KS_INDEXER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HBASE_INDEXER",
          "items" : [ {
            "name" : "hbase_indexer_java_heapsize",
            "value" : "362807296"
          } ]
        } ],
        "items" : [ {
          "name" : "hbase_service",
          "value" : "hbase"
        }, {
          "name" : "solr_service",
          "value" : "solr"
        } ]
      },
      "roles" : [ {
        "name" : "ks_indexer-HBASE_INDEXER-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "HBASE_INDEXER",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "32jh2gkmlf15ppmlca0hbcn7j"
          } ]
        }
      } ],
      "displayName" : "Key-Value Store Indexer"
    }, {
      "name" : "spark_on_yarn",
      "type" : "SPARK_ON_YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SPARK_YARN_HISTORY_SERVER",
          "items" : [ {
            "name" : "history_server_max_heapsize",
            "value" : "471859200"
          } ]
        } ],
        "items" : [ {
          "name" : "yarn_service",
          "value" : "yarn"
        } ]
      },
      "roles" : [ {
        "name" : "spar40365358-SPARK_YARN_HISTORY_SERVER-a9385a6b69af2022eb6fd16b6",
        "type" : "SPARK_YARN_HISTORY_SERVER",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "efb6144l6cp72cjsgrs0d5kqj"
          } ]
        }
      }, {
        "name" : "spark_on_yarn-GATEWAY-26e828bd331a7f59c757cf402af1894b",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-03a485749529c242e"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "spark_on_yarn-GATEWAY-7d34c2516a78bf9457c6cfa22d8b3643",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-06cba7a9024616d9d"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "spark_on_yarn-GATEWAY-a174f43d04c2c5b46d7df37a62439544",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-006cddb5b330a28f9"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "spark_on_yarn-GATEWAY-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "spark_on_yarn-GATEWAY-bcdeb026f4a31e7fecdd3b789bc807d7",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-07a5115443329aa57"
        },
        "config" : {
          "items" : [ ]
        }
      } ],
      "displayName" : "Spark"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "362807296"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "755"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3170683699"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "2449473536"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "1073741824"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "362807296"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "Q776xKijlWnbIkNw3tpxFDoScsP7jQ"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "zN8VsXvh15VOCnP42rmwCNLH15044b"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "n19x1zR7CfIhNFJ35DeZsoNLXCp24i"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-26e828bd331a7f59c757cf402af1894b",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-03a485749529c242e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "q0tqvagc9jehn189e0p2nm3s"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-7d34c2516a78bf9457c6cfa22d8b3643",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-06cba7a9024616d9d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6mz1netwzxbe5i2k259mndf3n"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-a174f43d04c2c5b46d7df37a62439544",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-006cddb5b330a28f9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9wkgghns9fd284zdf8jdrlex6"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-bcdeb026f4a31e7fecdd3b789bc807d7",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-07a5115443329aa57"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ehbbqqn10s2dki17bb4uc6kgd"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-a174f43d04c2c5b46d7df37a62439544",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-006cddb5b330a28f9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8jgr4e1s5b14t22d2g24dod7h"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4uzty5rnd7tp26oe91bmc38a6"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-26e828bd331a7f59c757cf402af1894b",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-03a485749529c242e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3by8rqxq7z9mbmapnowd7ghb1"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-a174f43d04c2c5b46d7df37a62439544",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-006cddb5b330a28f9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "be0cd1xeszfps4vfikydljoyj"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ba7xq2zvr9kdufcc5nzzcpgej"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-a174f43d04c2c5b46d7df37a62439544",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-006cddb5b330a28f9"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "101"
          }, {
            "name" : "role_jceks_password",
            "value" : "1oimplchkkn7dctz87t2ww4sf"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "59"
          }, {
            "name" : "role_jceks_password",
            "value" : "b67jn8fnrpf6hinxpc7p4tnk8"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "362807296"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "362807296"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2082052505"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "350"
          } ]
        } ],
        "items" : [ {
          "name" : "hbase_service",
          "value" : "hbase"
        }, {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-34-74.us-west-2.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "password"
        }, {
          "name" : "hive_metastore_database_user",
          "value" : "root"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "spark_on_yarn_service",
          "value" : "spark_on_yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-26e828bd331a7f59c757cf402af1894b",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-03a485749529c242e"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-7d34c2516a78bf9457c6cfa22d8b3643",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-06cba7a9024616d9d"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-a174f43d04c2c5b46d7df37a62439544",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-006cddb5b330a28f9"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-bcdeb026f4a31e7fecdd3b789bc807d7",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-07a5115443329aa57"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "134oxvrsgdj8o68lcvp5hny07"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5h9y77kzettgsczgziav6ive4"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "hbase",
      "type" : "HBASE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "MASTER",
          "items" : [ {
            "name" : "hbase_master_java_heapsize",
            "value" : "362807296"
          } ]
        }, {
          "roleType" : "REGIONSERVER",
          "items" : [ {
            "name" : "hbase_regionserver_java_heapsize",
            "value" : "1884291072"
          } ]
        } ],
        "items" : [ {
          "name" : "hbase_enable_indexing",
          "value" : "true"
        }, {
          "name" : "hbase_enable_replication",
          "value" : "true"
        }, {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hbase-MASTER-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "MASTER",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7fh6ov7shy5g980y8qpjb0rhn"
          } ]
        }
      }, {
        "name" : "hbase-REGIONSERVER-26e828bd331a7f59c757cf402af1894b",
        "type" : "REGIONSERVER",
        "hostRef" : {
          "hostId" : "i-03a485749529c242e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3k4s2oqwlkgbdyea97b77m85w"
          } ]
        }
      }, {
        "name" : "hbase-REGIONSERVER-7d34c2516a78bf9457c6cfa22d8b3643",
        "type" : "REGIONSERVER",
        "hostRef" : {
          "hostId" : "i-06cba7a9024616d9d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8grlbyoqp8d92881v3blga3uu"
          } ]
        }
      }, {
        "name" : "hbase-REGIONSERVER-a174f43d04c2c5b46d7df37a62439544",
        "type" : "REGIONSERVER",
        "hostRef" : {
          "hostId" : "i-006cddb5b330a28f9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c4khzja9110b9a3dayrixv0ti"
          } ]
        }
      }, {
        "name" : "hbase-REGIONSERVER-bcdeb026f4a31e7fecdd3b789bc807d7",
        "type" : "REGIONSERVER",
        "hostRef" : {
          "hostId" : "i-07a5115443329aa57"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1majrusbql4pzvzp671jg9e5z"
          } ]
        }
      } ],
      "displayName" : "HBase"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "maxSessionTimeout",
            "value" : "60000"
          }, {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "362807296"
          } ]
        } ],
        "items" : [ {
          "name" : "zookeeper_canary_connection_timeout",
          "value" : "30000"
        }, {
          "name" : "zookeeper_canary_operation_timeout",
          "value" : "60000"
        }, {
          "name" : "zookeeper_canary_session_timeout",
          "value" : "60000"
        } ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-26e828bd331a7f59c757cf402af1894b",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-03a485749529c242e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b2f52bci6hl1ri1iykcvxsc1h"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-a174f43d04c2c5b46d7df37a62439544",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-006cddb5b330a28f9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5tkryaa7bl0ixpiu0lurg3v3x"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7vbwepr9y0bxtidck6gs4ouus"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-34-74.us-west-2.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "password"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "database_user",
          "value" : "root"
        }, {
          "name" : "hbase_service",
          "value" : "hbase"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-a9385a6b69af2022eb6fd16b6db129c4"
        }, {
          "name" : "impala_service",
          "value" : "impala"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "solr_service",
          "value" : "solr"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "acro1uoil2ctzl9ys8lsw5fvu"
          }, {
            "name" : "secret_key",
            "value" : "F6uPYks94YIT6KvCPtFCjtsHCP5Ejm"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "solr",
      "type" : "SOLR",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SOLR_SERVER",
          "items" : [ {
            "name" : "solr_java_direct_memory_size",
            "value" : "471859200"
          }, {
            "name" : "solr_java_heapsize",
            "value" : "362807296"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "solr-SOLR_SERVER-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "SOLR_SERVER",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b3ey8ol5kjh9rp0dc6senlqks"
          } ]
        }
      } ],
      "displayName" : "Solr"
    }, {
      "name" : "impala",
      "type" : "IMPALA",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "CATALOGSERVER",
          "items" : [ {
            "name" : "catalogd_embedded_jvm_heapsize",
            "value" : "362807296"
          } ]
        }, {
          "roleType" : "IMPALAD",
          "items" : [ {
            "name" : "enable_audit_event_log",
            "value" : "true"
          }, {
            "name" : "impalad_memory_limit",
            "value" : "2449473536"
          }, {
            "name" : "scratch_dirs",
            "value" : "/impala/impalad"
          } ]
        } ],
        "items" : [ {
          "name" : "hbase_service",
          "value" : "hbase"
        }, {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "llama_am_ha_zk_auth_secret_key",
          "value" : "SF2cTZiVYm3W0EAGqV8SBW6DEqeXPN"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        } ]
      },
      "roles" : [ {
        "name" : "impala-CATALOGSERVER-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "CATALOGSERVER",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ddxddl7ubyymbjdu04cwjfohs"
          } ]
        }
      }, {
        "name" : "impala-IMPALAD-26e828bd331a7f59c757cf402af1894b",
        "type" : "IMPALAD",
        "hostRef" : {
          "hostId" : "i-03a485749529c242e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3di0449f72dpcnp5hdjcn1oob"
          } ]
        }
      }, {
        "name" : "impala-IMPALAD-7d34c2516a78bf9457c6cfa22d8b3643",
        "type" : "IMPALAD",
        "hostRef" : {
          "hostId" : "i-06cba7a9024616d9d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d45k1k2id6kgwy4w8hvb5k2c4"
          } ]
        }
      }, {
        "name" : "impala-IMPALAD-a174f43d04c2c5b46d7df37a62439544",
        "type" : "IMPALAD",
        "hostRef" : {
          "hostId" : "i-006cddb5b330a28f9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cazfpnjiba0fz7p0py3cf3ar9"
          } ]
        }
      }, {
        "name" : "impala-IMPALAD-bcdeb026f4a31e7fecdd3b789bc807d7",
        "type" : "IMPALAD",
        "hostRef" : {
          "hostId" : "i-07a5115443329aa57"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "49khumji5qgyc9b1nxzg6q2x7"
          } ]
        }
      }, {
        "name" : "impala-STATESTORE-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "STATESTORE",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2f30p28f7yjp91hhatxtks54q"
          } ]
        }
      } ],
      "displayName" : "Impala"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "8"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "362807296"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "2336"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "362807296"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "2336"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "4"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "hCIx9cqf1H6ZUWzj1vknCuaKq70c9K"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3jhaygfq7th5h84urve8j1pkw"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-26e828bd331a7f59c757cf402af1894b",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-03a485749529c242e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b5148qn7raqdxpdqs3vnn0ogt"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-7d34c2516a78bf9457c6cfa22d8b3643",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-06cba7a9024616d9d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7scz1zwxvey4obxwwlqk725e7"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-a174f43d04c2c5b46d7df37a62439544",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-006cddb5b330a28f9"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6rf3fr4yeo1k96f9bt97dhs1k"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-bcdeb026f4a31e7fecdd3b789bc807d7",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-07a5115443329aa57"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d811kn7kqq0ibi52iqtb2eqqd"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-a9385a6b69af2022eb6fd16b6db129c4",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-0044109a7e6427166"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "98"
          }, {
            "name" : "role_jceks_password",
            "value" : "acegzba23fsn9fxxmjugcptqs"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-0044109a7e6427166",
    "ipAddress" : "172.31.34.74",
    "hostname" : "ip-172-31-34-74.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-006cddb5b330a28f9",
    "ipAddress" : "172.31.41.122",
    "hostname" : "ip-172-31-41-122.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-03a485749529c242e",
    "ipAddress" : "172.31.43.123",
    "hostname" : "ip-172-31-43-123.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-07a5115443329aa57",
    "ipAddress" : "172.31.44.74",
    "hostname" : "ip-172-31-44-74.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-06cba7a9024616d9d",
    "ipAddress" : "172.31.44.9",
    "hostname" : "ip-172-31-44-9.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-a9385a6b69af2022eb6fd16b6db129c4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "7cf5a2896d471abb1355cf52f4b762cc00f46641079b9464fa0792443980c4ac",
    "pwSalt" : -6728422641233234362,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-a9385a6b69af2022eb6fd16b6db129c4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "7ddf0f3f0085259b77c14a875db62257e94dac726e82a15a92c10307364a8252",
    "pwSalt" : 3876525676850776491,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-NAVIGATOR-a9385a6b69af2022eb6fd16b6db129c4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "9a79c50f9c3ce8ee8175cd31e828b7b1b1340dae3dbb15f84b4fae7ee618db64",
    "pwSalt" : 7816172393933102714,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-NAVIGATORMETASERVER-a9385a6b69af2022eb6fd16b6db129c4",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "efc8832d6d687d1ffaa4b168f27285b3aa234147d72a76d85ce68d177c7765f9",
    "pwSalt" : -4081670370140575991,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-a9385a6b69af2022eb6fd16b6db129c4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "1f705dc8552e77a2f7afed6971f85f9c7a9d084110ef6bcae5ab17309666adc2",
    "pwSalt" : -7403812023418820923,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-a9385a6b69af2022eb6fd16b6db129c4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "392ee75b32eebf9bad8600825e5dea01ff1e161f47d12ec3245f06dcf9baac61",
    "pwSalt" : -373992284017482289,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "d386ff729f052da385d2f2c5a95341bb17ad0d6bba475180c0ed595ea3ccd6c4",
    "pwSalt" : 2770731978866086445,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "ce47cb2d572d67070248c34ff704af48c574c87ab3d354ff9f2b73c4fb79abcc",
    "pwSalt" : -8626641853625797441,
    "pwLogin" : true
  }, {
    "name" : "vlin3",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "c4a590c8e1140d21462011adac2f2ac022f1221d58a694beead5385c42b27a59",
    "pwSalt" : -3753274917037681572,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.9.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170330-1814",
    "gitHash" : "822da28bff818f57fc1bfc3eafe3a550300ef1b0",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "362807296"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "NAVIGATOR",
        "items" : [ {
          "name" : "navigator_database_host",
          "value" : "ip-172-31-34-74.us-west-2.compute.internal"
        }, {
          "name" : "navigator_database_name",
          "value" : "nas"
        }, {
          "name" : "navigator_database_password",
          "value" : "password"
        }, {
          "name" : "navigator_database_user",
          "value" : "root"
        }, {
          "name" : "navigator_heapsize",
          "value" : "362807296"
        } ]
      }, {
        "roleType" : "NAVIGATORMETASERVER",
        "items" : [ {
          "name" : "nav_metaserver_database_host",
          "value" : "ip-172-31-34-74.us-west-2.compute.internal"
        }, {
          "name" : "nav_metaserver_database_name",
          "value" : "nms"
        }, {
          "name" : "nav_metaserver_database_password",
          "value" : "password"
        }, {
          "name" : "nav_metaserver_database_user",
          "value" : "root"
        }, {
          "name" : "navigator_heapsize",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-34-74.us-west-2.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "password"
        }, {
          "name" : "headlamp_database_user",
          "value" : "root"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "362807296"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-a9385a6b69af2022eb6fd16b6db129c4",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-0044109a7e6427166"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "dv2x2nxepub32fgsakaoco766"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-a9385a6b69af2022eb6fd16b6db129c4",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-0044109a7e6427166"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7eykjmr5v03aufsqjpup12jew"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-a9385a6b69af2022eb6fd16b6db129c4",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-0044109a7e6427166"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "petxjw8g4gpapyin5kb4mpdw"
        } ]
      }
    }, {
      "name" : "mgmt-NAVIGATOR-a9385a6b69af2022eb6fd16b6db129c4",
      "type" : "NAVIGATOR",
      "hostRef" : {
        "hostId" : "i-0044109a7e6427166"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2w9011omjces8qair1615hbww"
        } ]
      }
    }, {
      "name" : "mgmt-NAVIGATORMETASERVER-a9385a6b69af2022eb6fd16b6db129c4",
      "type" : "NAVIGATORMETASERVER",
      "hostRef" : {
        "hostId" : "i-0044109a7e6427166"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "aro1jbvjn6epv8gtl30z0em5i"
        }, {
          "name" : "unexpected_exits_thresholds",
          "value" : "{\"warning\":\"never\",\"critical\":\"never\"}"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-a9385a6b69af2022eb6fd16b6db129c4",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-0044109a7e6427166"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "370salks0oe07m5dk5qjtntq4"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-a9385a6b69af2022eb6fd16b6db129c4",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-0044109a7e6427166"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2d9rpi0p1eu5ke67rb2ctnhw6"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/22/2012 9:20"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}[root@ip-172-31-34-74 ~]# 
```