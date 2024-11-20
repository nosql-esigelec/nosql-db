# MongoDB Workshop Documentation

## Introduction

Welcome to the MongoDB workshop! In this session, you will learn how to set up a MongoDB environment using Docker and connect to it using both the Mongo Express web interface and the MongoDB shell.

## Prerequisites

- Docker and Docker Compose installed on your system
- Basic understanding of Docker concepts and commands

## MongoDB Setup with Docker
1. **Clone this reop**:
   ```bash
   git clone https://github.com/nosql-esigelec/nosql-db
   ```
2. **Move to the current folder**
   ```bash
   cd training/getting_started_mongo/
   ```
3. **Start Mongo Express and MongoDB Shell**:

   We will use Docker Compose setup our mongo Database and Mongo Express. The `docker-compose.yml` file defines the services that will be started. Run the following command to start the services defined in the `docker-compose.yml` file:

   ```sh
   docker-compose up -d mongo-server mongo-express
   ```
  > Before running this command, you need to download `docker-compose.yml` and the 
4. **Accessing Mongo Express(Optionnal)**:

   Open a web browser and navigate to `http://localhost:8081`. Log in using the username `admin` and the password `pass`.
   > That's just visual client to manage your database, you can use it to create, update, delete and read data from your database. We won't use it in this workshop.
## MongoDB Basics

We will use the MongoDB shell to connect to our MongoDB instance and perform some basic operations.

1. **Connecting to MongoDB with Shell**:

   To connect to your MongoDB instance with the shell, execute the following command:

   ```sh
   docker exec -it mongo-server mongosh --authenticationDatabase admin -u root -p example
   ```

The output should look like this:

   ![Alt text](mongo-data/output-shell.png) 

Exit from the shell using the `exit` command.

2. **Copy the data to you container**

   ```sh
   docker cp mongo-data/ mongo-server:/
   #docker cp <path-to-file> <container-name>:<path-to-destination>
   ```
   Let's check if the data is copied to the container
   ```sh
   docker exec -it mongo-server ls /mongo-data
   ```

If everything is ok, you can start the first workshop open the file [mongo-basics.md](mongo-basics.md) and follow the instructions.

## MongoDB with Python

We will use the Jupyter Notebook to connect to our MongoDB instance and perform some operations in an application context.

### Connect to jupyter using the service jupyter
```sh
docker-compose up jupyter
``` 
Open the link starting by `http://localhost:8888` in a web browser.


Now you can open the notebook `mongo-python.ipynb` located in the directory `work` and follow the instructions.

## MongoDB Atlas connection
   For connecting to MongoDB Atlas, use:

   ```sh
   docker exec -it mongo-server mongosh "mongodb+srv://user:password@serial-techos.hxiqgqy.mongodb.net/"
   ```

   Replace `user` and `password` with your actual MongoDB Atlas credentials.
   
The output should look like this:
   
   ```sh
   Atlas atlas-jx27t2-shard-0 [primary] test>
   ```
## Conclusion

Congratulations! You have successfully set up and connected to MongoDB using Docker. You now have a working environment to explore and manage MongoDB databases.
