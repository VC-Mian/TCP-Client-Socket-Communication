# TCP Client-Server Socket Communication

## Overview
A simple TCP client-server application built in C++ that demonstrates basic network socket programming. The server listens for client connections and echoes back any received messages.

## Features
- **Server**: Listens on a specified port and accepts multiple client connections
- **Client**: Connects to server, sends user input, and displays server responses
- **Echo functionality**: Server receives messages and sends them back to the client
- **Interactive client**: Allows continuous messaging until user enters `/QUIT`

## How It Works
1. **Server** binds to a port and listens for incoming connections
2. **Client** connects to server using IP address and port
3. Client sends user-typed messages to server
4. Server receives the message and echoes it back
5. Client displays the server response
6. Process repeats until client sends `/QUIT` command

## Technologies Used
- C++
- TCP/IP sockets
- POSIX socket libraries (`sys/socket.h`, `arpa/inet.h`, `netinet/in.h`)

## What I Learned
- TCP socket creation and configuration
- Client-server connection establishment
- Send/receive operations with proper buffer management
- Socket cleanup and connection termination
- Basic network protocol implementation

## Usage
```bash
# Compile
g++ -o server server.cpp
g++ -o client client.cpp

# Run server (example: port 8080)
./server 8080

# Run client (example: connect to localhost on port 8080)
./client 127.0.0.1 8080
