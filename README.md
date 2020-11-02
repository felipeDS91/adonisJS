<h1 align="center">
  <img
    alt="Logo"
    src="https://res.cloudinary.com/dixtjpk8s/image/upload/v1604355092/Projects/Adonis_acl71g.png" width="600px"
  />
</h1>

<h3 align="center">
  Project management API developed with AdonisJS V4 (Rocketseat bonus module)
</h3>

<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/felipeDS91/adonisJS">

  <a href="https://www.linkedin.com/in/felipe-douglas-dev/" target="_blank" rel="noopener noreferrer">
    <img alt="Made by" src="https://img.shields.io/badge/made%20by-felipe%20douglas-%20">
  </a>
  
  <img alt="Repository size" src="https://img.shields.io/github/repo-size/felipeDS91/adonisJS">

  <a href="https://github.com/felipeDS91/adonisJS/commits/main">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/felipeDS91/adonisJS">
  </a>

  <a href="https://github.com/felipeDS91/whatsapp-api/issues">
    <img alt="Repository issues" src="https://img.shields.io/github/issues/felipeDS91/adonisJS">
  </a>

  <img alt="GitHub" src="https://img.shields.io/github/license/felipeDS91/adonisJS">
</p>

<p align="center">
  <a href="#-about-the-project">About the project</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-technologies">Technologies</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-getting-started">Getting started</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;  
  <a href="#-license">License</a>
</p>

<p id="insomniaButton" align="center">
  <a href="https://insomnia.rest/run/?label=adonisJS&uri=https%3A%2F%2Fgithub.com%2FfelipeDS91%2FadonisJS%2Fblob%2Fmain%2FInsomnia.json" target="_blank">
    <img src="https://insomnia.rest/images/run.svg" alt="Run in Insomnia">
  </a>
</p>

## 👨🏻‍💻 About the project

This is an API Rest to manage project and tasks where I have learned about the main features in AdonisJS.

The main topics covered were:
-	Concept and structure
-	Setting ESlint
-	Database (Lucid ORM)
-	User registration
-	JWT Auth
-	Recover password
-	Send e-mail
-	Reset password
-	File upload
-	Show files (static route)
-	Creating models
-	Relations
-	CRUD
-	Validator
-	Handle exception
-	Internationalization
-	Pagination
-	Hook
-	Queue using Redis (Kue)
-	Setting Sentry
-	Deal with CORS
-	Database transaction


## 💻 Getting started

Import the `Insomnia.json` on Insomnia App or click on [Run in Insomnia](#insomniaButton) button

### Requirements

- [Docker](https://www.docker.com/)
- [Node](https://nodejs.org/en/download/)
- [NPM](https://www.npmjs.com/get-npm)
- [ADONIS](https://adonisjs.com/docs/4.1/installation)


**Clone the project and access the folder**

```bash
$ git clone https://github.com/felipeDS91/adonisJS.git && cd adonisJS
```

**Follow the steps below**

```bash
# Install the dependencies
$ npm install

# Creates a docker container for REDIS
$ docker run --name redis -p6379:6379 -d redis:alpine

# Creates a docker container or use your own mysql installation (changes the password)
$ docker run --name adonis  -e MYSQL_ROOT_PASSWORD="mysql_password" -p 3306:3306 -d mysql:5.7.30

# Creates a new mysql user (changes the username and password)
# To connect with mysql database you can use a tool like DBeaver for example
$ CREATE USER 'docker'@'localhost' IDENTIFIED BY 'docker';

# Create a database
$ CREATE DATABASE adonis;

# Give privileges for the created user 
$ GRANT ALL PRIVILEGES ON adonis.* TO 'docker'@'localhost';

# Refresh the privileges
$ FLUSH PRIVILEGES

# Make a copy of '.env.example' to '.env'
# and set with YOUR environment variables
$ cp .env.example .env

# Run the migrations
$ adonis migration:run

# Run this command to start the server in development mode
$ adonis serve --dev

# If you want, rRun this command to start the kue worker
$ adonis kue:listen

# Well done, project is started!
```


## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Made with 💜&nbsp; by Felipe Douglas 👋 [See my linkedin](https://www.linkedin.com/in/felipe-douglas-dev/)
