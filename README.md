
Todo App.

*******************
HOW TO RUN THE APP:

download code folder.

CD into "client" and type "npm install" and then "npm start" - this starts the client app

CD into "server" and type "npm install" and then " Node server.js" to start the server
*******************************


***********
These are the dependencies for the backend: express mongoose cors dotenv
***********

Backend the folder is named server
When you create the folder. In the command line. You type NPM init –y to create the package.Json file. 



The main control for the backend is the server.js file
Here the connection to the host and the database takes place. The express is used for creating routes. I created the routes.js file to have a cleaner server.js file. The routes.js file contains all the routes for the application. That is the routes for creating, reading, updating and deleting the todo application

The Models
This is the structure that you want to use to store data in the database. It is a todo app so I want to save the title of the todo which is a string and the state of completion which is a Boolean (true or false).

The Controllers
This is the engine of the application. The functions that handles the CRUD resides here. Then it stores the data to the database (Todo). 
Req.body and req.params. Here req means request. This data is coming from the frontend application. The params denoted with “:id” is the additional information in the url. 
Example : http://localhost:8000/updatetodo/605c79df7acb382b608df4a6
The Id is the bolded alpha-numeric string. It will be sent as a params to the backend.

 const todos = await Todo.find({}).sort({ _id: -1 });

This code retrieves data from the database. That is the .find({}) then the .sort({ _id: -1}) rearrange the data so that the last entry displays at the top of the list of items to do.

Testing
For the test, I used mocha and supertest, testing the entire CRUD endpoint to make sure it is working well
