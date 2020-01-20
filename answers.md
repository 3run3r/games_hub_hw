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

### Questions

1. What is responsible for defining the routes of the `games` resource?

Games Router (using function defined in Create Router)

2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?

Client is responsible for views and rendering of the web app, Server is responsible for setting up db.

3. What are the the responsibilities of server.js?

Sets up the web server and connects to the created DB.

4. What are the responsibilities of the `gamesRouter`?

Invoking createRouter function passing the data required as an argument. it will then be used to create restful routes

5. What process does the the client (front-end) use to communicate with the server?

within GamesService, a baseURL is defined which routes to the server port.

6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs

it's an object that has some indications on what to do with the response of the fetch function.

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?

routes that make use of CR and D of CRUD.

8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?

it allows to connect to and manipulate data from a db

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

Add to your diagram the dataflow for removing a game.
