## Mongo

# Install/Uninstall MongoDb
https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/


# Start Mongo db

```
sudo service mongod start

```
# Check Mongo Logs

```
tail -100f /var/log/mongodb/mongod.log

```
# Mongo config

```
/etc/mongod.conf 

```
# Stop Mongo

```
sudo service mongod stop

```
# Restart Mongo

```
sudo service mongod restart

```
# Begin using mongodb

```
mongo --host 127.0.0.1:27017
```