# go-ddd-cart
sample ddd shopping cart, work in progress.

would love help to continue to make this a working ddd example with at lease a few boundaries and proper golang "best practices".  There is a lot more to do, and lots of refactor my "Janky" code.

project structure

application

client

db

domain

infrastructure

model

shared

the current  infra repo test uses dynamodb local, although it could easily use a mock using the provided interface.

to setup the dynamo db local requirements to run the tests, download this file: https://s3.us-west-2.amazonaws.com/dynamodb-local/dynamodb_local_latest.zip

then take only the DynamoDBLocal_lib folder from there, and past that folder into the db/dynamodb_local_latest folder, which will give you the core files but also use the needed static schema.  

Before running the tests you will then go to the db/dynamodb_local_lastest folder and run the following java commmand to start/load the db info memtory: java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb
