# Reading 08 - API's

## API Design Best Practices

1. What does REST stand for?
  Representation State Transfer

2. REST APIs are designed around a ____.
  Architectural approach to design web services.

3. What is an identifer of a resource? Give an example.
  URL that is differential and relates to its resource (object, data or service)
  ie.https://adventure-works.com/orders/1

4. What are the most common HTTP verbs?
  GET, POST, PUT, PATCH, DELETE
5. What should the URIs be based on?
  Nouns (resource= object, data, or service)
6. Give an example of a good URI.
  https://adventure-works.com/orders

7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
  BAD THING= AVOID. Chatty web API's expose miniscule resources. "MORE REQUESTS, BIGGER THE LOAD".

8. What status code does a successful GET request return?
  HTTP status code 200

9. What status code does an unsuccessful GET request return?
  return 404 (Not Found)
10. What status code does a successful POST request return?
  HTTP status code 201
11. What status code does a successful DELETE request return?
  HTTP status code 204

[<==BACK](README.md)