To run locally

Requirements: MongoDBCommunnityServer
https://www.mongodb.com/download-center/community

You can download the MongoDB Community Server from the MongoDB download page. The download is a zip file. Unzip the contents, change the folder name to "mongodb", and move it to your users home directory. From there, create a "mongodb-data" directory in your user directory to store the database data.
You can start the server using the following command. Make sure to swap out "/Users/Leo/" with the correct path to your users home directory.

/Users/Leo/mongodb/bin/mongod --dbpath=/Users/Leo/mongodb-data

1. git clone
2. cd nodejs-taskapp
3. delete package-lock.json
4. run npm i or yarn
5. create config directory in root of project with test.env and dev.env files with the env variables listed below
6. npm run dev or yarn run dev

To run jest test suite run npm run test or yarn run test

If you want a GUI for your database use either Robo3t or MongoDB Compass.

Make sure to set environment variables for PORT, SENDGRID_API_KEY, JWT_SECRET, MONGODB_URL in a Config directory at the root of your project. Inside Config directory add test.env and dev.env each with those 4 variables.

1) PORT=3000
2) SEND_GRID_API_KEY= get your own api key
3) JWT_SECRET= can be any password
4) For development MONGODB_URL= MONGODB_URL=mongodb://127.0.0.1:27017/taskapp

To deploy:
Set the same environment variables for heroku/dokku except the PORT variable can be left out.
Heroku Environment variables can be set through the command line or directly on heroku.com.
Dokku environments variables can be set from the command line only.
dokku config:set appname KEY=value KEY_2=value2 KEY_3=value3

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/9736846b31eae2710b6c#?env%5BTask%20Manager%20API%20(dev)%5D=W3siZGVzY3JpcHRpb24iOnsiY29udGVudCI6IiIsInR5cGUiOiJ0ZXh0L3BsYWluIn0sInZhbHVlIjoibG9jYWxob3N0OjMwMDAiLCJrZXkiOiJ1cmwiLCJlbmFibGVkIjp0cnVlfSx7InZhbHVlIjoiZXlKaGJHY2lPaUpJVXpJMU5pSXNJblI1Y0NJNklrcFhWQ0o5LmV5SmZhV1FpT2lJMVkyRTFOR05oWkRCa01qVTRNak5sT1ROa05UTmtZbVVpTENKcFlYUWlPakUxTlRRek56ZzNNeko5LlJEY1Q3c2V4d0NYZWh5Y3RwTDV2WG9HUDQxSW5KQ1ZSQVlmRzFMSjBEa0EiLCJrZXkiOiJhdXRoVG9rZW4iLCJlbmFibGVkIjp0cnVlfV0=)

Original repo with commit history at https://github.com/leopolicastro/node-course
