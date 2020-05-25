README
========
https://www.npmjs.com/package/dynamodb-admin

For an overview of DynamoDB Local please refer to the documentation at http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Tools.DynamoDBLocal.html



Release Notes
-----------------------------

2017-04-13 (1.11.119)

  * Add TTL implementation
  * Update aws libs to 1.11.119

2017-01-24 (1.11.86)

  * Implement waiters() method in LocalDynamoDBClient
  * Update aws libs to 1.11.86
  * Enable WARN logging for SQLite


2016-05-17_1.0

  * Bug fix for Query validation preventing primary key attributes in query filter expressions

Running DynamoDB Local
---------------------------------------------------------------

java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb
npm install dynamodb-admin -g
export DYNAMO_ENDPOINT=http://localhost:8000
dynamodb-admin

For more information on available options, run with the -help option:

  java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -help
