# Lecture: Basic commands

**Obs**
- The explain() output has changed in MongoDB 4.2. Specifically, a new section called explain.queryPlanner.optimizedPipeline has been added to the output. You can read about it in the optimizedPipeline docs.


## Usefull shell helpers

### User management
```shell
db.createUser()
db.dropuser()
```

### Collection management
```shell
db.renameCollection()
db.collection.createIndex()
db.collection.drop()
```

### Database management
```shell
db.dropDatabase()
db.createCollection()
```

### Database management
```shell
db.serverStatus()
```

### Creating index with Database Command:
```shell
db.runCommand(
  { "createIndexes": <collection> },
  { "indexes": [
    {
      "key": { "product": 1 }
    },
    { "name": "name_index" }
    ]
  }
)
```

### Creating index with shell helper:
```shell
db.<collection>.createIndex(
  { "product": 1 },
  { "name": "name_index" }
)
```

### Introspect a shell helper:
```bash
db.<collection>.createIndex
```
