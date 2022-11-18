# Nodejs Tutorial

## Local mongodb

    docker run -d --name mongodb -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=admin 

    # Install mongodb-client on ubuntu. Now you are inside the mongo db running on your local. Run below commands to check dbs in it.
    asrivastava@dev:~$ mongo -u admin -p --authenticationDatabase "admin"
    MongoDB shell version v3.6.8
    Enter password:
    connecting to: mongodb://127.0.0.1:27017
    Implicit session: session { "id" : UUID("d1628850-b737-40c0-ac06-594074c06c45") }
    MongoDB server version: 6.0.2
    WARNING: shell and server versions do not match
    Server has startup warnings:
    <.
    .
    strips
    .
    .>

    > show dbs
    admin         0.000GB
    config        0.000GB
    local         0.000GB
    > use globomantics
    switched to db globomantics
    > show dbs
    admin         0.000GB
    config        0.000GB
    globomantics  0.000GB
    local         0.000GB

### Load the session inside the local mongo db from sessions.json

From browser hit localhost:4000/admin
Now the session details will be pulled from local mongodb database.


