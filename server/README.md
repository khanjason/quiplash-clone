## Quip API's

### Getting started
To contribute or use the code in `server/` you need will to do a few things.  

Create a .env file in the root of `server/` with the following information:  
``` 
DB_URL_DEV=your-dev-db 
PORT_DEV=your-dev-port

DB_URL_TEST=your-test-db
PORT_TEST=your-test-port

```

To get the [prompts](https://github.com/nyu-software-engineering/quip-thinking/blob/master/prompts/prompts.csv) on your local machine, `cd server/` and run the command `npm run updateDB`.



### Real-Time App
The server is implemented using [socket-io](https://npmjs.com/package/socket.io). There are a number of event listeners which can be found in the [socket-config.js](https://github.com/nyu-software-engineering/quip-thinking/blob/master/server/socket/socket-config.js).  

To **start** : `npm run sock`.  
To **test**: `npm run sockTest`.  
The test cases are also a good reference for how to use the socket.io events on the client side.  


### API's
The following api's can be used to access the database.

To **test**: `npm run test`  
To **start**: `npm run start`

##### POST '/prompt/create-prompt'

body {  
question: \< question \>  
}  

Takes form input with body above, creates a new prompt and adds it to the database.


##### GET '/prompt/get-prompt'

Returns a random prompt from the database.
 
