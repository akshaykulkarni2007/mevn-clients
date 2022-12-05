# Big Language Solutions MEVN Project

This is simple MEVN project which allows users to perform CRUD operations on `clients` and associated `providers` for the clients. Deployed [netlify](https://prismatic-genie-08330c.netlify.app/). API server is deployed on [render](https://mevn-clients-server.onrender.com)

Client and server are totally detached from one another. Node-Express server only provides REST API by connecting with MongoDB database. Vue frontend consumes this service. It is designed this way so that server can be reused with any frontend.
<br/>

## Local develpment environment

---

Clone repository:

```
 git clone --recurse-submodules https://github.com/akshaykulkarni2007/mevn-clients
 git submodule update --remote --merge

```

### Environment variables

.env file with all environment variables is not pushed to repository. Create file named .env in both `client` and `server` folders. The values to be put in the files are provided separately in email.
<br/>

### Starting local development environment

Run `npm run deps` in `root` directory **OR** `npm install` in `root` directory, `client` directory and `server` directory.

Run folowing command from root directory to start client and server simultaneously:

```
npm run dev
```

### Starting client and server separatly

#### Starting Express Server

Run following commands to start local server and connect to MongoDB database:

```
cd server
npm run dev
```

#### Starting Vue client

Run following commands to start Vue client:

```
cd client
npm run dev
```

### Seeding sample data and purging database

Run following commands for seeding database with sample data:

```
npm run seed
```

Purge the database with this command:

```
npm run purge
```

**These commands can be run from root and server directory**

**It is recommended to purge the data before seeding it to avoid errors due to duplicate keys.**
<br/><br/>

## Building the project

---

Run following commands to build client project:

```
cd client
npm run build
```

<br/>

## Repository

---

Both client and server code bases are maintained as submodules to main repository in root directory. This allows different teams to work with code that they actually need instead of cloning entire repository. The main repository in root folder contains configuration to start client+server development environment. It can be used by fullstack developers as they need both client and server running on local machine. Frontend developers and backend developers can work only with client and server submodules respectively.

Each submodule can be treated as independent repo.

To pull latest changes in each submodule, run following command in root directory:

```
git submodule update --remote --merge
```

<br/>

## SWAGGER

Local swagger docs can be accessed on `/api/docs`. [local](http://localhost:5000/api/docs).

<br/><br/>

## Future improvements

---

- better form validations
- better error handling on client
- clear form on submission
- better security on server
