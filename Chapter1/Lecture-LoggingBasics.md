# Logging basics

- The logging output has changed in MongoDB 4.2. If you're interested, you can find more information in the 4.2 release notes for Logging & Diagnostics.

## Lecture instructions

- Get the logging components
```shell
mongo admin --host 192.168.103.100:27000 -u m103-admin -p m103-pass --eval '
  db.getLogComponents()
'
```

- Change the logging level
```shell
mongo admin --host 192.168.103.100:27000 -u m103-admin -p m103-pass --eval '
  db.setLogLevel(0, "index")
'
```

- View the logs through the Mongo shell
```shel
db.adminCommand({ "getLog": "global" })
```

- View the logs through the command line
```shell
tail -f /data/db/mongod.log
```

- Update a document
```shell
mongo admin --host 192.168.103.100:27000 -u m103-admin -p m103-pass --eval '
  db.products.update( { "sku" : 6902667 }, { $set : { "salePrice" : 39.99} } )
'
```

- Look for instructions in the log file with **grep**
```shell
grep -i 'update' /data/db/mongod.log
```
