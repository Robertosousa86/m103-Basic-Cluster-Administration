# Lab: Configuration file

## Problem:

**Launch a mongod instance in the IDE terminal with a configuration file:**

1. Write the configuration file. There should be an empty configuration file in your IDE File Editor, where you can specify options in YAML.

As a reminder, here are the requirements of your mongod instance:

- run on port 27000
- authentication is enabled

2. When your config file is complete, launch mongod with the ```--config``` command line option:

```bash
mongod --config mongod.conf
```

or using the ```-f``` option:

```bash
mongod -f mongod.conf
```

Once mongod is running, open a new Terminal window and use the following command to create an admin user. You will need to create this user in order to validate your work.

```bash
mongo admin --host localhost:27000 --eval '
  db.createUser({
    user: "m103-admin",
    pwd: "m103-pass",
    roles: [
      {role: "root", db: "admin"}
    ]
  })
```

Click "Run Tests" to run a suite of tests that will check the configuration of your mongod. The results of these tests will let you know which steps you've yet to complete.