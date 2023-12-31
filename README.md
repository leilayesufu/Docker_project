## demo app -Docker

This demo app shows a simple user profile app set up using 
- index.html with pure js and css styles
- nodejs backend with express module
- mongodb for data storage

All components are docker-based

### Blog
The full project can be seen on my blog https://leilayesufu.hashnode.dev/dockerize-a-nodejs-and-mongodb-application-and-push-it-to-amazon-ecr



#### To start the application With Docker Compose

Step 1: start mongodb and mongo-express

    docker-compose -f docker-compose.yaml up
    
_You can access the mongo-express under localhost:8080 from your browser_
    
Step 2: in mongo-express UI - create a new database "my-db"

Step 3: in mongo-express UI - create a new collection "users" in the database "my-db"       
    
Step 4: start node server 

    cd app
    npm install
    node server.js
    
Step 5: access the nodejs application from browser 

    http://localhost:3030

#### To build a docker image from the application

    docker build -t my-app:1.0 .       
    
The dot "." at the end of the command denotes location of the Dockerfile.
