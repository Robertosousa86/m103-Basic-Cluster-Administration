# Lecture: The Mongod

*Note: If you are running mongod on windows OS then please specify the --port option to avoid any undesired behavior.*

## Lecture instructions

- Launch mongod in the first shell:
```bash
mongod
```

- Connect to the Mongo shell in the second shell:
```bash
mongo
```

- To create a new collection:
```bash
db.createCollection("employees")
```

- Try to connect back to Mongo shell, without specifying a port:
```bash
use admin
db.shutdownServer()
exit
```
