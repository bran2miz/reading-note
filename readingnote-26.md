# Reading 12 - CRUD

Status Codes Based On REST Methods

1. In your own words, describe what each group of status code represents:
100’s = Like a status update, it will produce a response to tell the client that it will try to deal with the request.

200’s = When the code is successful, it will produce 200 response codes.
300’s = The 300 codes are codes that produce messages that tell the client that the request is not available in the requested destination.
400’s = Client related error messages that happens when there is an bad request that is trying to be sent to the server.
500’s = Server related error messages.

2. What is a status code 202?
  *Accepted*- asynchronous processing. Gives the promise that it will accept the request, but it will be fulfilled in the future.

3. What is a status code 308?
  *Permanent Redirect*- can access the resource if the client correctly inputs the newly created URL

4. What code would you use if an update didn’t return data to a client?
  204 *No Content*

5. What code would you use if a resource used to exist but no longer does?
  410 *Gone*

6. What is the ‘Forbidden’ status code?
  403 *Forbidden*- no authorization is required but the client still does not have permission to access the resource.

Build A REST API With Node.js, Express, & MongoDB - Quick - First 20 minutes

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
  We want to put it into an environment variable, so that when we deploy our backend, anyone can put their MongoDB string in the .env file and make the application work.

2. What is middleware?
  Code that runs when the server gets a request but before it gets passed in the routers.

3. What does app.use(express.json()) do?
  Uses any middleware (app.use). Express.json accepts .json as a body instead of a post element or get element.

4. What does the /:id mean in a route?
  Parameter and can access by using req.param.id

5. What is the difference between PUT and PATCH?
  Patch update whatever the user passes. Put updates all the information of the db all at once.

6. How do you make a default value in a schema?
  default: < value>.now

7. What does a 500 error status code mean?
  Error on the server which caused the transaction not to work. Nothing to do with the client.

8. What is the difference between a status 200 and a status 201?
  201 status means it successfully created an object; it is also a more specific way of defining the positive result of the code working properly. By default, if you don't define the status, it will send the 200 code for success.

## Things I want to know more about

**Permanent Redirect Code**

[<==BACK](README.md)
