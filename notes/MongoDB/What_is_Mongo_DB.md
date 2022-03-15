
![MongoDB](https://webassets.mongodb.com/_com_assets/cms/mongodb_logo1-76twgcu2dm.png)

# M001 
## What is MongoDB?
- A NoSQL documentDatabase ( Does not use legacy approach of relative databases.)
- Data is not stored in rows / columns
- Data is stored as documents in collection
- Data is however stored in a structured way

#### Atlas 
- Atlast is a built for wide range of applications with MongoDB as Core.
- It has many tools and services which uses MongoDB
- Atlas users can deploy clusters
- Clusters : Groups of servers which stores data. They are configured in a replica set. 
- Instance : Single instance of storage. ( In this case )
- Few connected instances with same data is called Replica Set
- The same data is stored in replica sets and this helps to ensure that data is lost even if one of the instance gets corrupted

### Terminal Application for Ubuntu
https://downloads.mongodb.com/compass/mongodb-mongosh_1.1.9_amd64.deb

### How are Documents stored?
- Data stored in Json ( Javscript Standard Object Notation)
- Key value seperated by :
- Keys are also called Fields in MonoDB
-Sub-Document : Json Within a Json

### Drawbacks of storing in JSON
- Text based storage and hence slow
- Json readable format is space consuming
- Json has limited datatypes

##### To overcome there, BSON was invented. 
- Binary representation to store data in JSON Format

#### MongoDB uses BSON (Binary Standard Object Notation)