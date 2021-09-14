# Lecture: Launching mongod

## Problem:

**Launch your own mongod process in the IDE terminal:**

1. From your IDE terminal, launch a mongod instance that listens for connections on port 27000.
If you run into any issues, you can always type Ctrl-C in the terminal where mongod is running to stop it. Then you can restart it with a new configuration.
When the process is running, you can open a new tab in the IDE to use the Mongo shell, but this is optional for this assignment. 

2. Once you've run the proper commands, click "Run Tests" to run a suite of tests that will check the configuration of mongod. The results of these tests will let you know which steps you've yet to complete.

## Answer

```bash
mongod --port 27000
```
start mongod and run test.