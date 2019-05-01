# Backup Mongo in Docker Container

## Mongo Dump

```closure
docker run --rm --link <name-of-container>:mongo -v <path-to-save-backup-at>:/backup mongo bash -c ‘mongodump --out /backup --host mongo:27017’
```

## Mongo Restore

```closure
docker run --rm --link <name-of-container>:mongo -v <path-to-save-backup-at>:/backup mongo bash -c ‘mongorestore /backup --host mongo:27017’
```
