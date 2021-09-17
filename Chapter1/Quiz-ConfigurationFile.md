# Quiz: configuration file

## Problem

- Consider the following:

**mongod --dbpath /data/db --logpath /data/logs --replSet M103 --bind_ip '127.0.0.1,192.168.103.100' --keyFile /data/keyfile --fork**

Which of the following represents a configuration file equivalent to the command line options?

## Answer

```bash
storage:
  dbPath: "/data/db"
systemLog:
  destination: file
  path: "/data/logs"
replication:
  replSetName: "M103"
net:
  bindIp: "127.0.0.1,192.168.103.100"
security:
  keyFile: "/data/keyfile"
processManagement:
  fork: true
  ```