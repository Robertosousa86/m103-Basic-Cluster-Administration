# Logging basics

## Problem:
- Which of the following operations can be used to access the logs?

## Answer

- Running ```db.adminCommand({ "getLog": "global" })``` from the Mongo shell
This operation can be used to access logs from the Mongo shell.

- Running ```tail -f <path-to-log-file>``` from the command line
This operation can be used to access logs from the command line.