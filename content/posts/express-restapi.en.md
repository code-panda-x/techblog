---
title: "Rest API with Express.JS"
date: 2022-02-20T13:37:22-06:00
tags: ["Web Application", "API", "HTTP", "JavaScript", "Express"]
categories: ["General Tech"]
slug: "express-restapi"
subtitle: "Build your API with Express.JS"
description: "Build your API with Express.JS"
keywords: 
- REST API
- Express
- JavaScript
---

## To include packages/files

### Include packages: packages are from package.json

    const express = require('express');
    const router = express.Router();
    		router.get('/', (req, res) => res.send('Profile route'));

    const jwt = require('jsonwebtoken');

### Inlucde route/file:

```
// db.js module.exports = connectDB;
// In server.js
const connectDB = require('./config/db')
connectDB();
```

## File return

```
module.exports = connectDB;
module.exports = router;
```

## Try catch

```
const connectDB = async () => {
    try{
        await mongoose.connect(db, {
            useNewUrlParser: true
        });

        console.log('MongoDB Connected!');
    } catch(err){
        console.error(err.message);
        // Exit process with failure
        process.exit(1);
    }
}
```

## Build Express API:

## Hierarchy

```
// server.js
const express = require('express');
const app = express()

app.get('/', (req, res) => res.send('API Running'));
// Define Routes
app.use('/api/users', require('./routes/api/users'));
app.use('/api/auth', require('./routes/api/auth'));
app.use('/api/profile', require('./routes/api/profile'));
app.use('/api/posts', require('./routes/api/posts'));

const PORT = process.env.PORT || 5000;
//app.listen() starts a port and host to listen to incoming requests from a client.
app.listen(PORT, () => console.log(`Server started on port ${PORT}`));

////////////////////////////////////////////////////////////////////////
// profile.js
const express = require('express');
const router = express.Router();

// Postman --Get request--> http://localhost:5000/api/profile
// res.send --> 'Profile route' --> Postman
router.get('/', (req, res) => res.send('Profile route'));

module.exports = router;
```

## Notes regarding REST API

1. Requests are third party requests sent to our sever(such as Postman)

2. Router.post/get/put/delete: it is how we handle incoming requests ( requests sent to our server)

   ```
   router.post/get/put/delete('/', auth, async (req, res) => { do some response here});
   ```

3. Express.Router() use req,res to handle requests

   ```
   req: contains POST request JSON body
   	const {name, email, password} = req.body
   res: is whatever info the server sends back
   	res.status(500).send('Server error');
   	res.status(400).json({errors: [{msg: 'User already exists'}]});
   	res.json({ msg: 'User deleted' });
   ```

## More about REST API

POST:

- Requester sends info and data to a server
- POST request has a body (JSON) and a header (Content-Type, application/json , x-auth-token)

GET:

- **DON'T have a body** When a request is sent to our sever's route, our server responds a message back (router.get('/', (req, res) => res.send('Profile route'));)
- Can have a header (x-auth-token)

PUT:

- Work like a POST, have body & header. But it meanly used to update a resource

Delete:

- Delete a resource in DB, usually require a x-auth-token in the header
