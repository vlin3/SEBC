### Challenges Setup

## List the cloud provider you are using (AWS, GCE, Azure, other)
```
AWS
```

## List your instances by their IP address and DNS name
```
172.31.26.189	ip-172-31-26-189.us-west-2.compute.internal	52.27.1.204		ec2-52-27-1-204.us-west-2.compute.amazonaws.com
172.31.25.239	ip-172-31-25-239.us-west-2.compute.internal	52.33.223.75	ec2-52-33-223-75.us-west-2.compute.amazonaws.com
172.31.16.149	ip-172-31-16-149.us-west-2.compute.internal	34.209.56.78	ec2-34-209-56-78.us-west-2.compute.amazonaws.com
172.31.21.196	ip-172-31-21-196.us-west-2.compute.internal	35.166.123.231	ec2-35-166-123-231.us-west-2.compute.amazonaws.com
172.31.17.180	ip-172-31-17-180.us-west-2.compute.internal	52.38.227.128	ec2-52-38-227-128.us-west-2.compute.amazonaws.com
```

## List the Linux release you are using
```
[root@ip-172-31-26-189 source]# cat /etc/centos-release
CentOS release 6.5 (Final)
```

## List the file system capacity for the first node
```
[root@ip-172-31-26-189 source]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  761M   28G   3% /
tmpfs            15G     0   15G   0% /dev/shm
```

## List the command and output for yum repolist enabled
```
[root@ip-172-31-26-189 source]# yum repolist enabled
Loaded plugins: fastestmirror, presto
Determining fastest mirrors
 * base: mirror.chpc.utah.edu
 * extras: mirrors.unifiedlayer.com
 * updates: denver.gaminghost.co
repo id                                                repo name                                                         status
base                                                   CentOS-6 - Base                                                   6,706
extras                                                 CentOS-6 - Extras                                                    64
updates                                                CentOS-6 - Updates                                                  270
repolist: 7,040
```

## List the /etc/passwd entries for zhou and chen
```
zhou:x:2800:2800::/home/zhou:/bin/bash
chen:x:2900:2900::/home/chen:/bin/bash
```

## List the /etc/group entries for shanghai and beijing
```
shanghai:x:500:chen
beijing:x:501:zhou
zhou:x:2800:
chen:x:2900:
```
