![Image](https://webassets.mongodb.com/_com_assets/cms/mongodb_logo1-76twgcu2dm.png)

# Importing and Exporting in Mongo DB

- to a local machine
- to a different system
- from a different system
- import from local machine

 ### Json
-  mongoimport  --uri "< Atlas Ccluster URL>"
	- 
- mongoexport  --uri "< Atlas Ccluster URL>"

### Bson
- mongodump  --uri "< Atlas Ccluster URL>"
- mongorestore --uri "< Atlas Ccluster URL>"
	- --drop dump : Helps in avoiding conflicts with duplicate entires as it drops the existing columns while doing the restore

URI : Uniform Resource Identifier

User SRV Connection string format to establish a secure connection

Example of url : 

	mongodb+srv://user.password@clusterURI.mongodb.net/satabase

### Examples codes
	mongodump --uri "mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies"
    
	mongoexport --uri="mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies" --collection=sales --out=sales.json

	mongorestore --uri "mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies"  --drop dump

	mongoimport --uri="mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies" --drop sales.json