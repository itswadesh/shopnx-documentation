---
title: Installation Instructions
date: 2017-07-25 06:40:12
---
### Softwares

- NodeJS (Web Server) (https://nodejs.org/en/)
- MongoDB (Database) (https://www.mongodb.com/)
  
### Start mongodb in a separate shell
  In Windows operating system we can start it by opening the following file
  ``` bash
  C:/Program Files/MongoDB/Server/3.2/bin/mongod.exe
  ```  

### Run the following 2 commands
  This will install the required node dependencies and start the Server at http://localhost:4200
  ``` bash
npm i
npm run dev
  ```  
### Building files for production server
This will generate both client and server files inside dist directory which can be directly copied to production server
  ``` bash
npm run prod
  ```  
### Run at server
  ``` bash
npm start
  ```  
  <br/>
  <br/>