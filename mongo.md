### MangoDB CookBook

```
// connect mongodb
mongo mongodb://username:password@remote.host.com:27017/mydb

// connect with more options
mongo mongodb://username:password@remote.host.com:27017/mydb?authSource=admin&readPreference=secondary&ssl=true

// show all databases 
show dbs; 

// switch database default use test  
use your_db;

// add super user
use admin;
db.createUser({user:"root", pwd:"your_pwd", roles:[{role:"root", db:"admin" }] });

// auth user success if return 1
db.auth("root","your_pwd");


```
### Type
- Talble/Collection/Row/Document/Col/Field
- Primary Key/ObjectId/Index
- Embeded Table/Embeded Document/Array

