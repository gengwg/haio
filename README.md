Install single node Hadoop on CentOS 7 with Ansible

## Prerequisites

* Vagrant 
```
$ vagrant --version
Vagrant 1.8.5
```

* Ansible
```
$ ansible --version
ansible 2.2.0.0
```

## Test

### Verify Hadoop Services is up
http://192.168.33.12:50070/

### Put a file

```
[hadoop@hadoop ~]$ hdfs dfs -mkdir /user
[hadoop@hadoop ~]$ hdfs dfs -mkdir /user/hadoop
[hadoop@hadoop ~]$ hdfs dfs -put /var/log/boot.log
```

```
Permission  Owner Group Size  Last Modified Replication Block Size  Name
-rw-r--r--  hadoop  supergroup  6 B 7/31/2017, 11:43:49 AM  1 128 MB  boot.log
```

###  Verify applications for cluster
http://192.168.33.12:8088/cluster
