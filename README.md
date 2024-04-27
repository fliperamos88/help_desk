

# Help Desk Application

- Help Desk
  - [Description](#description)
  - [Tech Stack](#tech-stack)
  - [Installation](#installation)
  - [Login](#login)


## Description

### Tech Stack Help Desk Application
- Overview: Streamlines support ticket submission, management, and resolution.
- Features:
 - User Ticket Submission with file attachment.
 - Admin Ticket Management with assignment capability.
 - Seamless communication between users and admins.
 - Ticket tracking from submission to resolution.

## Tech Stack

This application was developed with the support of the following tools:

- Programming languages: [JavaScript](https://www.javascript.com)
- Libraries/Frameworks: [Express](https://expressjs.com), [React](https://react.dev), [Node.js](https://nodejs.org/en), [Bootstrap](https://getbootstrap.com), [Sequelize](https://sequelize.org/docs/v6/getting-started/)
- Database storage and management: [PostgreSQL](https://www.postgresql.org)

## Installation

### Package installation

To install all the packages on both the frontend and backend, run:

```shell
$ node run client
```

### Database

This application was developed using PostgreSQL database. To connect to the database, you'll need to create a [Sequelize](https://sequelize.org/docs/v6/getting-started/) instance. This can be achieved by renaming the .env-example file in the server directory to.env. Provide the connection parameters within each variable of the .env file. The config.js file, located in server/config, will read these variables and construct the Sequelize URI for you.

Database variables: POSTGRES_URL; POSTGRES_USER; POSTGRES_HOST; POSTGRES_PASSWORD; POSTGRES_DATABASE

### JWT Secret Key

After renaming the aforementioned .env file, assign a value to the SECRET_KEY variable, which JWT will use to sign the token generated.

### Front-end API class

The frontend interacts with the backend server through the wrapper class API located in client/src/helpers/GameAPI.js

Rename the second .env-example file located in the client directory to.env and define the base application URL to the variable REACT_APP_API_URL 

### Setting it live locally

After package installation and database connection, to set the application live, run the following command from the server directory: 

```shell
$ npm start
```

## Login

The following Admin/User have been pre-generated and can be used to login to the application as an Admin:

{"username": "Admin1", "password": "testpassword123"}

{"username": "Admin2", "password": "testpassword456"}

{"username": "Admin3", "password": "testpassword789"}

{"username": "Admin4", "password": "testpassword456"}

You can also register a new Admin  by executing a POST request with body {username, password} to {REACT_APP_API_URL}/api/auth/register
