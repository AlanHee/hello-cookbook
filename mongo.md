### MangoDB CookBook

```
// connect mongodb
mongo mongodb://username:password@remote.host.com:27017/mydb

// connect with more options
mongo mongodb://username:password@remote.host.com:27017/mydb?authSource=admin&readPreference=secondary&ssl=true

// show all databases 
show dbs 

// switch database default use test  
use your_db

// add super user
use admin
db.createUser({user:"root", pwd:"your_pwd", roles:[{role:"root", db:"admin" }] })

// auth user success if return 1
db.auth("root","your_pwd")

// craete collection(database)
use col_name

// insert recorde
db.col.insert({...})

// remove database
db.dropDatabase()

// update recorde
db.col.update({name:'alan'}, {$set:{age:18, case:'father'}})
// insert if update not math
db.col.update({...},{...},{upsert:true})
// update multipute recorde
db.col.update({...},{...},{multi:true})


// find recorde 
db.col.find().pretty()

// find recorde by AND 
db.col.find({... , ...}).pretty()
db.col.find({name:'alan', "age":18}).pretty()

// find recorde by OR 
db.col.find({$or:[{...},{...}]}).pretty()
db.col.find({$or:[{name:'walle'},{name:'eva'}]})

// find recorde by 
// $lt  less than
// $lte less and equal then
// $gt  grant then 
// $gte grant and equal then
// $ne  not equal
db.col.find({age: {$lt:22}})

// remove all
db.col.remove({})

```
### Type
- Talble/Collection/Row/Document/Col/Field
- Primary Key/ObjectId/Index
- Embeded Table/Embeded Document/Array

