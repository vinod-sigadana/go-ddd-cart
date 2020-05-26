## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Project Structure](#project-structure)
* [Setup](#setup)

## General info
This project needs assistance to continue to deplop additional Aggregate Roots following a shopping cart domain. There  is also a lot of code that  could be improved, some of it is  marked with //ToDo.
* This is a starter project of a Domain Driven Design implimentation using Go. The example emulates a typical shopping cart project, howver it is in the very beginnings and as of now only has the user aggregate root started.  
* Domain-driven design (DDD) is the concept that the structure and language of your code (class names, class methods, class variables) should match the business domain. For example, if your software processes loan applications, it might have classes such as LoanApplication and Customer, and methods such as AcceptOffer and Withdraw.
	
## Technologies
Project is created with:
* Go
* asdfsaf
* asdfaf
	
## Project Structure
The building blocks of this project include:
* application -- Defines the use cases the software is supposed to do and coordinates the domain objects to work out problems.  This layer is kept thin. It does not contain business rules or knowledge, but only coordinates tasks and delegates work to collaborations of domain objects in the next layer down.  It does not have state reflecting the business situation, but it can have state that reflects the progress of a task for the user or the program.
* client -- This is the top most layer, essentailly for example a rest service wrapper.  It is meant to wire up all of the depedencies for the application layer.  Handler is executed by AWS Lambda in the main function. Once the request is processed, it returns an Amazon API Gateway response object to AWS Lambda this is the aggregate for DynamoDBUserRepo entity.
* db --  This is where the data store is implimented. It uses DynamoDB Local and is currently used for the autommated testing.
* domain -- Responsible for representing concepts of the business, information about the business situation, and business rules.  State that reflects the business situation is controlled and used here, even though the technical details of storing it are delegated to the infrastructure.  This layer is the heart of business software.
* infrastructure -- Implimention of tech stack.
* model -- Domain Entities
* shared -- Shared logic


## Setup
* To run this, the current  infra repo test uses dynamodb local, although it could easily use a mock using the provided interface.
* To setup the dynamo db local requirements to run the tests, download this file: https://s3.us-west-2.amazonaws.com/dynamodb-local/dynamodb_local_latest.zip
* Then take only the DynamoDBLocal_lib folder from there, and past that folder into the db/dynamodb_local_latest folder, which will give you the core files but also use the needed static schema.  
* Before running the tests you will then go to the db/dynamodb_local_lastest folder and run the following java commmand to start/load the db info memtory: java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb project, install it locally using npm:

