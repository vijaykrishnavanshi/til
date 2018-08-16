# Secure Mongo using Authentication Strategy

Step 0: Check the status of mongo, if it is running.

```closure
sudo systemctl status mongod
```

Step 1: Start the mongo shell.

```closure
mongo
```

Step 2: use admin database, and create an admin user.

```closure
> use admin
> db.createUser(
>   {
>     user: "Admin",
>     pwd: "Admin'sSecurePassword",
>     roles: [ { role: "userAdminAnyDatabase", db: "admin" } ]
>   }
> )
```

Step 3: Make mongo to use authentication before allowing any access.
Make a copy on the conf file just to be safe and you can replace it when nothing works.

```closure
sudo cp /etc/mongod.conf /etc/backup-mongo.conf
sudo nano /etc/mongod.conf
```

Look for security section. Add the following

    security:
        authorization: "enabled"

Step 4: Restart mongo service.

```closure
sudo systemctl restart mongod
```

Check the status of the restarted service using

```closure
sudo systemctl status mongod
```

You can login as an admin user.

```closure
mongo -u Admin -p --authenticationDatabase admin
```
