## CMD - local 

use databaseName    - it will use database or create if not exist  
show collections    - show list of collections of current db 
db                  - show current db in use 
show dbs            - list of db


### Crud 
- Find 

-- _id:0 wihout id it will show values 
db.userInfoCollection.find()                      - all data 
db.userInfoCollection.find({name:"value"})        - query 
db.userInfoCollection.find().pretty()
db.userInfoCollection.find().limit(1) / db.userInfoCollection.findOne()                - limit the records show 
db.userInfoCollection.find().limit(1).skip(1)                - show specific position , basically it skip 1st record and as limit shows , so it show 2nd record only 
db.userInfoCollection.find(query , projection)   
-- Projection = ex: name:1 so it only output namve value and if name:0 in that case it will only outpout all fileds wihtout name        
db.userInfoCollection.find(query , fieldName:0)               -  outshow only projected values
