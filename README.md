# okytrihidayat
server.js

const express = require("express");
const mongoose = require("mongoose");

const app = express();

// DB Config
const db = require("./config/keys").mongoURI;

// Connect to MongoDB
mongoose
  .connect(db)
  .then(() => console.log("MongoDB Connected"))
  .catch(err => console.log(err));

app.get("/", (req, res) => res.send("salam buat kamu"));

const port = process.env.PORT || 3000;

app.listen(port, () => console.log(`Server running on port ${port}`));


kie terminal e

[nodemon] restarting due to changes...
[nodemon] restarting due to changes...
[nodemon] starting `node server.js`
(node:13408) DeprecationWarning: current URL string parser is deprecated, and
will be removed in a future version. To use the new parser, pass option { useNewUrlParser: true } to MongoClient.connect.
(node:13408) DeprecationWarning: current Server Discovery and Monitoring engine is deprecated, and will be removed in a future version. To use the new Server Discover and Monitoring engine, pass option { useUnifiedTopology: true } to
the MongoClient constructor.
Server running on port 3000
MongoNetworkError: failed to connect to server [ds233288.mlab.com:33288] on first connect [MongoError: Authentication failed.
    at Function._getError (C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\auth\scram.js:125:14)
    at C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\auth\scram.js:175:31
    at Connection.messageHandler (C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\connection\connect.js:334:5)
    at Connection.emit (events.js:210:5)
    at processMessage (C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\connection\connection.js:368:10)
    at Socket.<anonymous> (C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\connection\connection.js:537:15)
    at Socket.emit (events.js:210:5)
    at addChunk (_stream_readable.js:308:12)
    at readableAddChunk (_stream_readable.js:289:11)
    at Socket.Readable.push (_stream_readable.js:223:10)
    at TCP.onStreamRead (internal/stream_base_commons.js:182:23) {
  name: 'MongoError',
  [Symbol(mongoErrorContextSymbol)]: {}
}]
    at Pool.<anonymous> (C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\topologies\server.js:431:11)
    at Pool.emit (events.js:210:5)
    at C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\connection\pool.js:559:14
    at C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\connection\pool.js:973:11
    at callback (C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\connection\connect.js:109:5)
    at C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\connection\connect.js:352:21
    at C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\auth\auth_provider.js:66:11
    at C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\auth\scram.js:177:16
    at Connection.messageHandler (C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\connection\connect.js:334:5)
    at Connection.emit (events.js:210:5)
    at processMessage (C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\connection\connection.js:368:10)
    at Socket.<anonymous> (C:\Users\HP\Desktop\devconnector1\node_modules\mongodb\lib\core\connection\connection.js:537:15)
    at Socket.emit (events.js:210:5)
    at addChunk (_stream_readable.js:308:12)
    at readableAddChunk (_stream_readable.js:289:11)
    at Socket.Readable.push (_stream_readable.js:223:10) {
  name: 'MongoNetworkError',
  errorLabels: [ 'TransientTransactionError' ],
  [Symbol(mongoErrorContextSymbol)]: {}
}
