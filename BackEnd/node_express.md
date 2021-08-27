# Node Express notes

### Table of Contents
1. [Installing Packages](#installing-packages)
2. [Node Notes](#node-notes)
    * [Import Files](#import-external-files)
    * [Export Files](#export-from-a-file)
    * [Specify Database](#specify-database-for-prod-or-test)
    * [Query Database](#query-database)
3. [Express Notes](#express-notes)
    * [Connect Route File](#connect-app-to-routes-file)
4. [Springboard Notes](#springboard-notes)

Other Files:
1. [Python Flask](./python_flask)
2. [SQL](./sql)
3. [Copy Pasta](../copy_pasta)
---

# Installing Packages

#### Axios
    npm install axios

#### psycopg2
    npm install pg

#### Express
    npm install express

#### Nodemon (global install)
    npm install --global nodemon

---

#### Install dependencies
    npm install

---

# Node Notes

### Starting a Project with NPM
    cd my-project
    npm init -y

### Start Nodemon Server
    nodemon app.js

---

### Import external files
    const axios = require('axios');
    const usefulStuff = require("./usefulStuff");

#### Export from a file
    module.exports = {
        variable: aVariable,
        function: aFunction,
        Class: AClass
    };

---

#### Specify database for prod or test
    //Database setup.

    const { Client } = require("pg");

    let DB_URI;

    if (process.env.NODE_ENV === "test") {
        DB_URI = "postgresql:///users_test";
    } else {
        DB_URI = "postgresql:///users";
    }

    let db = new Client({
        connectionString: DB_URI
    });

    db.connect();

    module.exports = db;


#### When Testing Start file with
    process.env.NODE_ENV = 'test'

---

#### Query database
    const db = require("../db");

    router.get("/", async function (req, res, next) {
        try {
            const results = await db.query(`
                SELECT id, name, type FROM users
            `);

            return res.json(results.rows);
        }

        catch (err) {
            return next(err);
        }
    });


---

# Express Notes

### Express Scaffold
    const express = require("express");
    const app = express();

    // Parse request bodies for JSON
    app.use(express.json());

### Connect App to routes file
    const externalRoutes = require("./routes/external");
    app.use("/external", externalRoutes);

---

# Springboard Notes

 * #### [JS Promises (31.2)](http://curric.rithmschool.com/springboard/lectures/js-promises/)

* #### [JS Async Await (31.3)](http://curric.rithmschool.com/springboard/lectures/js-async/)

* #### [Node Intro (31.4)](http://curric.rithmschool.com/springboard/lectures/node-intro/)

* #### [Node Jest Testing (31.5)](http://curric.rithmschool.com/springboard/lectures/node-jest-testing/)

* #### [Express Intro (32.1)](http://curric.rithmschool.com/springboard/lectures/express-intro/)

* #### [Express Router, Middleware (32.2)](http://curric.rithmschool.com/springboard/lectures/express-router-middleware/)

* #### [Express PG Intro (35.1)](http://curric.rithmschool.com/springboard/lectures/express-pg-intro/)

* #### [Node Postgress Relationships (35.2)](http://curric.rithmschool.com/springboard/lectures/express-pg-relationships/)

* #### [Database OO Design Patterns (35.3)](http://curric.rithmschool.com/springboard/lectures/express-pg-oo/)

* #### [Hashing and JWTs with Node (36.1)](http://curric.rithmschool.com/springboard/lectures/express-hashing-jwts/)

* #### [Validation with JSONSchema (36.2)](http://curric.rithmschool.com/springboard/lectures/express-api-validation/)

* #### [Express Testing Practices (36.3)](http://curric.rithmschool.com/springboard/lectures/express-testing-practices/)

* #### [Node/Express Wrapup (36.4)](http://curric.rithmschool.com/springboard/lectures/express-wrapup/)