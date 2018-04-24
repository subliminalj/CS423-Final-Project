# CS423-Final-Project
Final Project for CS423 Client/Server Programming

Alexander Carlisle and Jay Hixson

Design a web client-server application which the server entity applies a cache server to serve a client. The client and the proxy cache can be coded with any programming languages in any Platform. In this project, you need three different machines Client, Cache server and Origin server which the processes are explained below:

The Origin Server can use Apache2 in one of the GENI machines applied in the slice you made before. Cache server code and Client code should be in 2 different GENI virtual machines (if you want to use an IDE in Windows then you can also have these two entities in your local machine and your teammate’s). The client code asks for a file from cache server. With the request that the client asks it will put the Epoch time of the machine in the header and sends it to the caches server. The cache code receives the request for the file and start checking in the directory if the file exists, cache sends the file to the client, but if the file does not exist in cache directory, then the cache will ask origin server for the file. Origin server will send the file to the cache and cache will save it in the directory and send it to the client. The cache webserver gets the Epoch time of the cache machine at the moment it receives a request from the client and at the moment it sends the file to the client and put it in the HTTP header and send it to the client.
