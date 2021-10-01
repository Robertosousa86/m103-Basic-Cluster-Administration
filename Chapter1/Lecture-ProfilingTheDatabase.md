# Lecture: Profiling the database

## Lecture instructions

**Note: The command `show collections` no longer lists the system.\*** **collections. It changed after version 4.0.**

- To list all of the collection names you can run this command:

```bash
db.runCommand({listCollections: 1})
```

- Get profiling level:

```shell
mongo newDB --host 192.168.103.100:27000 -u m103-admin -p m103-pass --authenticationDatabase admin --eval '
  db.getProfilingLevel()
'
```

- Set profiling level:

```shell
mongo newDB --host 192.168.103.100:27000 -u m103-admin -p m103-pass --authenticationDatabase admin --eval '
  db.setProfilingLevel(1)
'
```

- Show collections:

```shell
mongo newDB --host 192.168.103.100:27000 -u m103-admin -p m103-pass --authenticationDatabase admin --eval '
  db.getCollectionNames()
'
```

**Note: show collections only works from within the shell**

- Set slowms to 0:

```shell
mongo newDB --host 192.168.103.100:27000 -u m103-admin -p m103-pass --authenticationDatabase admin --eval '
  db.setProfilingLevel( 1, { slowms: 0 } )
'
```

- Insert one document into a new collection:

```shell
mongo newDB --host 192.168.103.100:27000 -u m103-admin -p m103-pass --authenticationDatabase admin --eval '
  db.new_collection.insert( { "a": 1 } )
'
```

- Get profiling data from system.profile:

```shell
mongo newDB --host 192.168.103.100:27000 -u m103-admin -p m103-pass --authenticationDatabase admin --eval '
  db.system.profile.find().pretty()
```
