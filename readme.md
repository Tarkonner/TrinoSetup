# Description
This project is a setup for Trino to run locally on a PC in Docker. Trino is a federation query engine that lets one make one query, send it to multiple databases. The databases can be both SQL and NoSQL. This lets the users for example make joins across tables.
The setup is made to make Read Only queries. 
The setup is made to automatically mount the Trino container with the catalogs and rules setup.

# Setup
## Use connectors
To make a connection to a database, a catalog needs to be added to the catalog folder in the project. How it is written changes after what kind of database you want to connect to (Documentation: https://trino.io/docs/current/connector.html). Remember that the file should be a .properties type. The name of the connecters can't have uppercase letters.
Remember to restart the project if connectors were added while trino was running.
To see if the catalogs setup is set up correctly, get into Trino and call: “SHOW CATALOGS;”. That should show a list of the type of databases you have set up. 

## Run Solution
Call command in the project folder:
docker compose up -d

# SQL
There are 2 way of making SQL
Write directly to Trino with the Command prompt. Use the Get into Trino command to get into Trino where you can write the queries.
Use a 3-party SQL engine of choice. Connect to port 8080 with the platform.
- if using Jetbrain datagrip, you can connect to the port. Set Authentication to User & Password. Set user to "as" and leave password blank.

# Commands
Get into Trino:
docker exec -it trino trino

# Links
https://trino.io/ 

