


A node server and a node client. The server implements the REST API and the client tests the rest api.


The server creates a sqlite database for 'users'. The server runs on localhost:8085.
The client tests the server with a series of HTTP request to the rest API points. 
The client checks the response body of the request to make sure server acted as expected.
The server has seven api points, and the client makes seven tests.
The sever api points are;

get '/api/'
Gets the entire collection

get '/api/:id'
Gets a user in the collection by the id 

put '/api/'
Replaces the collection with the one recived.

put '/api/:id'
Replaces the user in the collection by the id

post '/api/'
Adds the new user to the collection.

delete '/api/'
Deletes the entire collection.

delete '/api/:id'
Deletes the user with the specified id. 



The client tests are;

#1 Check that an inital GET collection request is empty.
#2 Check that two POST collection request will insert the two items into the collection.
#3 Check that a PUT collection request with two items in a collection will replace the current collection with this new collection.
#4 Checks that a DELETE collection request will remove all items from the collection. 
#5 Check that a GET item request will return the specific item from the collection.
#6 Check that a PUT item request will update the specific item in a collection.
#7 Check that a DELETE item request will delete a specific item from the colleciton. 

(After test 4, client runs tests 2 and 3 to re-populate the database so the later tests can run appropriately