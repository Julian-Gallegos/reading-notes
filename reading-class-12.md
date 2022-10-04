# Read Class 07: Topics on REST Status Codes and Building a Rest API with Node.js, Express, & MongoDB
  [Link back to main reading notes page](https://julian-gallegos.github.io/reading-notes/)


## Why this topic matters

These topics are important for building an effective CRUD app with REST


## Status Codes Based On REST Methods

source credit: [Which HTTP Status Code to Use for Every CRUD App](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)
   
   
   1. **In your own words, describe what each group of status code represents:**

      - 100’s = Informational codes for the client, for example, sending a message to confirm a request was just received .
      - 200’s = Success codes that confirm a request was accepted.
      - 300’s = Redirection codes that tell a client that their requested resource is unavailable at the requested information.
      - 400’s = Client error codes. The various ways an error occurred during client request that leaves the request invalid. Always an error on the client end and not from the recieving server.
      - 500’s = Server error codes. They indicate that some kind of error happened on the server end, such as an overwhelmed server not being able to process a request.

   
   2. **What is a status code 202?**

Asynchronous processing of a request. Doesn not mean the request was process, just that it met validation requirements at time of sending.


   3. **What is a status code 308?**

This tells the client to use another URL to access the resource and not use the current URL anymore.


   4. **What code would you use if an update didn’t return data to a client?**
     
Status code 204 (no content).


   5. **What code would you use if a resource used to exist but no longer does?**
   
Perhaps a 307, but I'm not sure.
   
   
   6. **What is the ‘Forbidden’ status code?**
   
Status code 403, client has no permissions to access resource.
   
   
## API Keys

   1. **Why do we need to pull our MongoDB database string out of our server and put it into our .env?**

The URL string will be different when deploying the server. While developing it is convenient to use localhost, but that won't be the proper URL when deployed. making the variable a .env variable means it is easy to add the variable later when deploying.
Additionally, while not as important in this context, .env can store sensitive data that the developer does not want to share, and is therefore a common target for .gitignore to hide the info.

   2. **What is middleware?**

Code that runs when the server gets a request, but before it gets passed to the server's routes


   3. **What does app.use(express.json()) do?**
   
This will let the server accept JSON as a body, instead of a POST element, or GET element, or etc.

   
   4. **What does the /:id mean in a route?**

This represents a parameter, and gives access to whatever the client passes in after the first `/`.


   6. What is the difference between PUT and PATCH?

`PUT` is a request to update data on the server. When it updates the data, instead of updating just the data that it passes, all the data for a given component in the server is updated.`PATCH` updates only what the client passes to the server.


   7. How do you make a default value in a schema?

use the `default` property within the key for a schema and initiate its value to whatever you want the default to be.


   8. What does a 500 error status code mean?

Internal server error that has nothing to do with the client making a mistake.


   9. What is the difference between a status 200 and a status 201?

Status 201 specifically means "successfully created an object" whereas status 200 broadly states that everything was successful.


## Things I want to know more about
   1. I just need more time to work with REST to wrap my head around it properly.
