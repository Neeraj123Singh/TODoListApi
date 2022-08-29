# todo-server-jwt

> Simple server app with JWT authentication that uses MongoDB, Node.js, and the Express web framework to provide a todo API.
Returns JSON data using standard REST requests. Can be used to support MEAN/MERN/MEVN full-stack apps.

This is just the server-side - no client-side GUI is included.



## Requirements

- A browser (e.g., Firefox or Chrome)
- A text editor (e.g., VS Code or Notepad++, or Chrome)
- Windows Powershell to run commands
- Node.js
- Atlas MongoDB hosting account (free)

## Run locally against your Atlas MongoDB

- Fork the repo
- Clone your repo down to your local machine
- Create config/default.json
- Install dependencies with `npm install`
- Run the server locally with `npm run dev`

## View local app in browser

- <http://localhost:5002>
- <http://localhost:5002/todo>


## Test requests with Postman

- Install [Postman](https://www.getpostman.com/)
- Additional details in following sections

Collection: "todo-server-jwt (local)"

- Set VERB + URI (and configure request if sending POST data)
- GET <http://localhost:5002/todo> - Send
- POST <http://localhost:5002/user> - set  Body / Raw / JSON & get back token
- POST <http://localhost:5002/todo> - set Auth / Bearer Token & Body / Raw / JSON / set "name" - Send
- DELETE <http://localhost:5002/todo/id> - set Auth / Bearer Token & copy id from post call and replace id - Send

Collection: "todo-server-jwt (heroku)"

- GET <https://todo-server-jwt-heroku-app.herokuapp.com/todo>
- POST <https://todo-server-jwt-heroku-app.herokuapp.com/user> - set  Body / Raw / JSON & get back token
- POST <https://todo-server-jwt-heroku-app.herokuapp.com/todo> - set Auth / Bearer Token & set Body / Raw / JSON - Send
- DELETE <https://todo-server-jwt-heroku-app.herokuapp.com/todo/id> - set Auth / Bearer Token copy id from post call and replace id - Send

## Create user with Postman (provides token)

1. POST <http://localhost:5002/user> - set Body / Raw / JSON - Send

