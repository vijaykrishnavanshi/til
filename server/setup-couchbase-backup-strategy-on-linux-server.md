# Setup [Couchbase](https://www.couchbase.com/) Backup Strategy on [Linux Server](https://en.wikipedia.org/wiki/Linux)

Step 0: Check if couchbase is running on sever.

```closure
service couchbase-server status
```

Step 1: place the script <https://github.com/vijaykrishnavanshi/server-stuff/blob/master/couchbase-backup.sh> to any particular path.

Step 2: Configure script variable according to your couchbase setup.

Step 3: Change the permission of the script:

```closure
chomd +x /path/to/script/couchbase-backup.sh
```

Step 4: Add a crontab that will run the script on a repeat interval.

```clojure
crontab -e
```

Step 5: Enter the following lines

```closure
# Couchbase Backup
00 00 * * * /path/to/script/couchbase-backup.sh
```

This will create a cronjob that will take the  backup at every midnight.

If you want to read more about crontab and the pattern in front. Read this - <https://www.computerhope.com/unix/ucrontab.htm>

If you want to test the different patterns, try this - <https://crontab.guru/>
