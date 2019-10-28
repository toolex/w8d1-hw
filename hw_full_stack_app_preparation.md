# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using Vue, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

![Overview of the tech stack and tooling with commands](images/tech_stack_with_commands.png)

*Overview of the tech stack and tooling with commands*

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

On paper

### Questions

1. What is responsible for defining the routes of the `games` resource?

create_router.js uses line 18 in server.js to difine the routes.

2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?

Client has the front-end things that relate to the client. The server folder handles movement of things between
the server and the database which is all local so its quite easy to move between.

3. What are the the responsibilities of server.js?

It is middleware. Sets up the express server and uses a body parser to identify json thats input through the form and sent back from the database.

4. What are the responsibilities of the `gamesRouter`?

Restful routes and sets the prefix of the url.

5. What process does the the client (front-end) use to communicate with the server?

Vue and event buses.

6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs.

It is an object that sends a payload that allows json encripted data to be sent with it.

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?



8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?




## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

Add to your diagram the dataflow for removing a game.
