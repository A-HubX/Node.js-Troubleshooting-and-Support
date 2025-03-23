This file demonstrates how to create a simple Node.js REST API using Express
Example:
# Initialize a new Node.js project
mkdir nodejs-api
cd nodejs-api
npm init -y

# Install Express
npm install express

# Create a basic API

index.js:
const express = require('express');
const app = express();

// Basic GET route
app.get('/', (req, res) => {
  res.send('Hello, Node.js API!');
});

// Start the server
app.listen(3000, () => {
  console.log('Server is running on http://localhost:3000');
});

To run the app, use:
node index.js
