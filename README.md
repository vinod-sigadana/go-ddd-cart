# go-ddd-cart
sample ddd shopping cart, work in progress.

the current  infra repo test uses dynamodb local, although it could easily use a mock using the provided interface.

to install dynamodb local go here https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.html

put it in a root folder called db.

then use this cmd java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb

it will load in memory and use port 8000 as default.
