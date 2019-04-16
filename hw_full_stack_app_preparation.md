# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using no frameworks, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

![Overview of the tech stack and tooling with commands](images/tech_stack_with_commands.png)

*Overview of the tech stack and tooling with commands*

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?
- create_router.js
2. What are the the responsibilities of server.js?
- Setting up and running the server.
3. What are the responsibilities of the `gamesRouter`?
- It contains the new router specific for displaying the list of games.
4. What process does the the client (front-end) use to communicate with the server?
- games.js's methods getData, postGame and deleteGame.
5. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs
- A method, which in this case sends json data via POST.
6. Which of the games API routes does the front-end application consume (i.e. make requests to)?
- The show, update and delete routes.
7. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?
- To create the non-relational database for the application.

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?
- So the update and delete routes would have a comparison base when changing the original entries.
