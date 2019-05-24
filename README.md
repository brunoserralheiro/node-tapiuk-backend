# TAPIUK



This application is a REST API usin Loopback 3, express middleware, and built in  AUTH

It is requered to have MongoDB and Node 8 installed on your computer.



0. on a CLI type:

npm i
npm start


Web server listening at: http://localhost:3030

Browse your REST API at http://localhost:3030/explorer





1. create TAPIUK database on MongoDB
2. create User collection
3. insert an user:
{
  "username":"...",
  "email":"",
  "password":""
}

4. browse on the swagger explorerr for User Post, or type  http://localhost:3030/explorer/#!/User/User_login on a browser to access the swagger explorer and login using the json object below

{
  "username":"...",
  "email":"",
  "password":""
}


5. the response should look like the below example:

{
  "id": "UVVWO6XYAv6Dma0foVeOUHV6BtIiBI2p82eF29Wl4pavTBbC9en08BLMUtPAAmj8",
  "ttl": 1209600,
  "created": "2019-05-24T15:31:17.865Z",
  "userId": "5caf692532e797229c964b3f"
}

copy  the "id" value and set the token on the right upper corner

6. browse on the swagger explorerr for Products POST , or  type http://localhost:3030/explorer/#!/products/products_find

7. type http://localhost:3030/explorer/#!/products/products_create on your browser to insert one product


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
