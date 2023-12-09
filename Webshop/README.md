# The Impenetrables

### How to run our code

1. Start the application
``` bash
docker-compose up --build
``` 
2. Since the database is not filled currently with books or users, we need to seed it. There’s a `seeder.js` script located inside the docker container backend, which prefills
   the database. Let this script run after the containers are all set up and running (the mongoDB container requires some time to be fully operational). The parameter --i is for filling the DB, the parameter --v for emptying it again. Use it whenever needed, but start as follows:
``` bash
docker exec -it backend -sh -c "node seeder.js --v && node seeder.js --i
``` 
