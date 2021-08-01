This project demonstrates the working of AWS SES and DynamoDB. The front-end is created using React-JS. The projecttakes (name, email, message) as input using front-end, save them in a DynamoDB and send it to the email-address mentioned in AWS SES.

The project structre is as following,

My-App
|_ backend
|_ client

backend - a folder consists of files demonstrating the service of AWS SES.
client -  a folder consist of files containing front-end and demonstrating service of AWS DynamoDB.

The folder is created using Amplify CLI.

to refer to amplify CLI - https://docs.amplify.aws/

To run this project,

First, create the node project using the npm commands,

Then, create an amplify CLI using your AWS credentials and command,

> amplify init

This command initialize your project on AWS cloud.

Then create a DynamoDB database using the command,

> amplify add storage

create a table named "formtable" with a schema as following,

(id: string, name: string, email:string, message: string) with id as a partition key.

Then create a REST API using the command,

> amplify add api

in the REST API create a lamda function names "formsunction".

copy the code of lambda function from client/amplify/backend/function/formfunction/App.js and paste it in your App.js file.

copy the code from client/src/App.js and paste it in your App.js file of node project.

run your node project using command,

> npm start 


 