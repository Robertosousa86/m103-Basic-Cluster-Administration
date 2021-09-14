# Lecture: Configuration file

**At 3:54 the speaker says "YAML stands for Yet Another Markup Language". This acronym has been updated to "YAML Ain't Markup Language".**

*See MongoDB documentation for more information about command line options and configuration file options.*

## Lecture instructions
*These lecture instructions are not meant to be reproduced in your environment. They reflect what you will see in the lecture video. However, they may point to non-existing resources and files.*

- Launch mongod using default configuration:
```bash
mongod
```

- Launch mongod with specified --dbpath and --logpath:
```bash
mongod --dbpath /data/db --logpath /data/log/mongod.log
```

- Launch mongod and fork the process:
```bash
mongod --dbpath /data/db --logpath /data/log/mongod.log --fork
```

- Launch mongod with many configuration options:

**_Note that all "ssl" options have been edited to use "tls" instead. As of MongoDB 4.2, options using "ssl" have been deprecated._**
```bash
mongod --dbpath /data/db --logpath /data/log/mongod.log --fork --replSet "M103" --keyFile /data/keyfile --bind_ip "127.0.0.1,192.168.103.100" --tlsMode requireTLS --tlsCAFile "/etc/tls/TLSCA.pem" --tlsCertificateKeyFile "/etc/tls/tls.pem"
```

- Example configuration file, with the same configuration options as above:

```bash
storage:
  dbPath: "/data/db"
systemLog:
  path: "/data/log/mongod.log"
  destination: "file"
replication:
  replSetName: M103
net:
  bindIp : "127.0.0.1,192.168.103.100"
tls:
  mode: "requireTLS"
  certificateKeyFile: "/etc/tls/tls.pem"
  CAFile: "/etc/tls/TLSCA.pem"
security:
  keyFile: "/data/keyfile"
processManagement:
  fork: true
```
