# Cosmos DB postman collection
This is a fork from [this original repo](https://github.com/MicrosoftCSA/documentdb-postman-collection). Main changes include:
1. Updated to the latest [API version](https://docs.microsoft.com/en-us/rest/api/cosmos-db/#supported-rest-api-versions) of 2018-12-31.
2. Focused more on document operations than database and collection operations.

## To install:
1. Import ```CosmosDBSQL.postman_collection.json``` to Postman collections.
2. Import ```CosmosDBSQLEnv.postman_environment.json``` to Postman environment.

## To Use:
1. Replace ```DocumentDBHost``` and ```DocumentDBMasterKey``` in the environment with your Cosmos DB settings.
2. Replace ```mydb```, ```mycol```, ```mydocid```, ```mydocpartitionkey``` in the url or headers of the request with your values. Note that these values in the url must be hardcoded. They can't be environment variables, as they are used in the script to compute the auth key. For example:
![Alt text](/cosmos.GIF?raw=true "Request")

3. Replace request body with your document or query content.
4. In the response header, you will see ```x-ms-request-charge```, which is the Cosmos DB RU (Request Unit) incurred by the request.
