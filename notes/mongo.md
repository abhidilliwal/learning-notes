# MongoDB notes 2018

### Connecting db

Generally to enter to mongodb we would just say: `mongo` in console.

### Create db and collections.

All the commands need to be entered on the console.

```bash
## list all the databases:
show databases;

## create a new database:
use example;
# > switched to db example

## now to make a new collection
db.newCollection.insertOne({name: 'yo'});

## to list all the collections in this current database:
show collections;
# > newCollection

## to list all the records in this collection:
db.newCollection.find();
# > { "_id" : ObjectId("5aad6eabd1d2d821260dc570"), "name" : "yo" }

## to pretty print:
db.newCollection.find().pretty();
# {
#    "_id" : ObjectId("5aad6f77d1d2d821260dc571"),
#    "name" : "Abhishek Dilliwal",
#    "age" : 31
#  }
```

