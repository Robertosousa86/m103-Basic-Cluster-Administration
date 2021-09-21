# Lecture: File structure

*Note: At 3:15, the instructor mistakenly says that the WiredTiger syncs the journal to disk every 50 milliseconds. On WiredTiger, the default journal commit interval is 100 milliseconds. For more information please refer our documentation.*

## Lecture instructions

- List --dbpath directory:
```bash
ls -l /data/db
```

- List diagnostics data directory:
```bash
ls -l /data/db/diagnostic.data
```

- List journal directory:
```
ls -l /data/db/journal
```

- List socket file:
```bash
ls /tmp/mongodb-27017.sock
```
