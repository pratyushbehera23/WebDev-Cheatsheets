# API

API Application Programming Interface - is a way for two computers (client, server) to talk to each-other (request, response)

The common API standard used by most mobile and web applications to talk to the servers is called REST (REpresentational State Transfer).
REST is kind of a set of rules that has been the common standard for building web API since 2000s.
An API that follow the REST standard is called a RESTful API.  ex: Twilio, Stripe, GMaps..

Web application (in your browser)  <->  RESTful API  <->  Web server  <->  Database  

A RESTful API orgainzes resources into a set of unique URIs(Uniform Resource Iddentifiers)
ex URIs: <https://example.com/api/v3/users> , <https://example.com/api/v3/products>
The URIs differentiate different types of resources on a server.

A client interacts with a resource by making a request to the endpoint for the resource over HTTP.
The request has a very specific format : POST/products HTTP/1.1
The URI is preceded by an HTTP verb (GET POST) which tells the server what we want to do with the resource. [POST - Create, GET - Read, PUT - Update, DELETE - Delete]
In the body of these requests, there could be an optional HTTP request body that contains a custom payload of data, usually encoded in JSON.

The server receives a request, processes it, and formats the result into a response.
The first line of the response contains the HTTP status code to tell the client what happened to the request. ex: HTTP/1.1 200 OK  [200-level - Success, 400-level - Something wrong with our request, 500-level - Something wrong at the server level]

A REST implementation should be stateless. ie. the two parties dont need to store any information about each-other, and every request and response (cycle) is independent from all others.

There are other popular API options like GraphQL and gRPC.

## GraphQL vs REST

GraphQL architecture is client-driven, REST is server-driven.
GraphQL orgainzed in terms of schema and type system, REST is endpoints.
GraphQL operations are query mutation subscription, REST are CRUD (Create Read Update Delete).

In a REST architecture, the client makes an HTTP request and data is send as an HTTP response,
while in GraphQL, the client requests data with queries.
