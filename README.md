# TAPIUK



This application is a REST API using Loopback 3, express middleware, and built in  AUTH

It is required to have MongoDB

the default datasource is

"mongoDS": {
    "host": "127.0.0.1",
    "port": 27017,
    "url": "",
    "database": "tapiuk",
    "password": "",
    "name": "mongoDS",
    "user": "",
    "connector": "mongodb"
  }

  if another path is configured, please update the above configuration on server\datasources.json file.

 Node 8 installed on your computer.



1. on a CLI type:

npm i
npm start


Web server listening at: http://localhost:3030

Browse your REST API at http://localhost:3030/explorer





2. create  database named tapiuk on MongoDB


3. create User collection on that DB.

OR alternatively  remove AUTH feature by commenting line 5 on server\boot\authentication.js

// server.enableAuth();


4. If using authentication plese insert an user directly on MongoDB User collection:
{
  "username":"myuser",
  "email":"myemail@example.com",
  "password":"123456"
}



5. browse on the swagger explorerr for User Post, or type  http://localhost:3030/explorer/#!/User/User_login on a browser to access the swagger explorer and login using the json object below

{
  "username":"myuser",
  "email":"myemail@example.com",
  "password":"123456"
}


6. the response should look like the below example:

{
  "id": "UVVWO6XYAv6Dma0foVeOUHV6BtIiBI2p82eF29Wl4pavTBbC9en08BLMUtPAAmj8",
  "ttl": 1209600,
  "created": "2019-05-24T15:31:17.865Z",
  "userId": "5caf692532e797229c964b3f"
}

copy  the "id" value and set the token on the right upper corner



7. browse on the swagger explorer for Products POST , type http://localhost:3030/explorer/#!/products/products_create on your browser to insert one product


  {
    "name": "string",
    "price": "",
    "inStock": false
  }




8. browse on the swagger explorer for Products GET, or type http://localhost:3030/explorer/#!/products/products_find on your browser


or checkout a client

(git clone) https://github.com/brunoserralheiro/angular-tapiuk-frontend



The client and the server are Work In Progress.

If more details are needed, please email bruno@serralheiro.eu

Thank you.


