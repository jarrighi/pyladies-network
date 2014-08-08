# Web 101 part 1 

## Introduction

The goal of today is to understand the components that go into building a web application.

We thought it would be a good idea to understand something about networking communicaiton and the interne before we go into that since this is a part of the communication between all of the pieces. 

A web application is a really fancy complex way to get data from around the internet onto your screen, usually (but not always) using a browser. In a really simple situation, the browser (which is a client) is making requests to a web server, recieving a response, and then displaying it. 

## Simple server client relationship. 

A server is a process that is listening for requests and has some kind of logic to create and return a response.
 
A client communicated with a server by sending requests and receiving responses.

Some examples of clients are browsers, curl command in terminal, mobile app.

Because there are a lot of varienty in servers, clients, and the hardware and operating systems they run on, we have protocols to help make sure they're communicating consistently.

Flesh out: Different protocols and protocol layers

Talk about IP, and addresses, what the transport layer is, and mention we'll com back to it later. 

## Building clients and servers with Python
We're going to start by building a simple server and client with python and then we will use them to send each other requests and responses

### Go through echo_server.py and echo_client.py

why we need socket, sys, and argparse

The socket library unsurprisingly allows us to create sockets to communicate over. It gives Python access to the system's socket interface. A socket is the part of a program where the communication happens. More about sockets… 

sys are argparse help us build the command line options. 

we need an address and port so that the client and server can communicate. And address corresponse to a particular device, and ports allow a device to control what traffic gets to them and then different processes can use different ports.

### Have everyone start up server script

```
$ python echo_server.py --port=9900
```
Then open another terminal and run the client

```
$ python echo_server.py --port=9900
```

### Questions to discuss
* Did it work?
* Why did we have to use two terminal windows?
* What would happen if the ports didn't match? 

### Continue, editing the scripts
Give everyone a chance to modify their server so that it does some thing more interesting. 
Try to get people making requests to other people's servers. 


## HTTP Protocol
Talk about http

* headers
* user agent
* http status codes

## Use cURL and requests module to view http responses



## Build HTTP server and client with Python

Now we're a lot closer to what web applications do, but most of them are much much much more complex. We'll talk about that second half, but before we do that, let's do a quick chat about transport of info and internet protocol, on the transport/network layer

## Packets, IP, etc
Talk about packets get around the internet
Do some demos, playing around with Traceroute and wireshark