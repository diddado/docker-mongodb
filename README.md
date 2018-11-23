MongoDB

You need a ```.env``` file to set the required parameters.  It should look like this:

```bash
COMPOSE_PROJECT_NAME=mongo4.0 # this should be unique for every version of mongo since the data volume will be persisted and will be named based on this value.
MONGO_VERSION=4.0
MONGO_PORT=27017
MONGO_INITDB_ROOT_USERNAME=YourMongoAdminUsername
MONGO_INITDB_ROOT_PASSWORD=YourMongoAdminPassword

MONGO_EXPRESS_PORT=8081
ME_CONFIG_MONGODB_ADMINUSERNAME=YourMongoExpressAdminUsername
ME_CONFIG_MONGODB_ADMINPASSWORD=YourMongoExpressAdminPassword

```

Run ```docker-compose up``` to start the container.

The configuration will default to the latest version if a .env file isn't created. 

You will run into data conflicts if you run multiple versions and don't set COMPOSE_PROJECT_NAME in the .env file.

