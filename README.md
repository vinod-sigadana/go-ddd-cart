# go-ddd-cart
sample ddd shopping cart, work in progress.

would love help to continue to make this a working ddd example with at lease a few boundaries and proper golang "best practices".  There is a lot more to do, and lots of refactor my "Janky" code.

project structure
application
client
db
-----this is where the dynamodb local stuff will go.
domain
infrastructure
model
shared

the current  infra repo test uses dynamodb local, although it could easily use a mock using the provided interface.

to install dynamodb local go here https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.html

put it in a root folder called db.

then use this cmd java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb

it will load in memory and use port 8000 as default.
