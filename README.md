# CSCI 333 (Computer Networks) Assignment 1
### Nurali Altair

## Description
Implementation of a basic and multi-client TCP Server using Socket API in Python.

## Features
- Entity 1: TCP Server sending constant response message back to the client.
- Entity 2: TCP Client that send message to the server.
- Entity 3: Multi-client TCP server with chat functionality using multi-threading.
- Entity 4: TCP client that authenticates with username and password

## Installation

### Prerequisites
- Python 3.9+
- SQLite
- bcrypt
- socket
- threading
- logging

## Running the Project

### Locally
- How to run the project locally (Task A).
  ```sh
  python nurali_altair_task1_sever.py  # To run TCP server
  python nurali_altair_task1_client.py  # To run TCP client
  ```
- Task B
  ```sh
  python db_population.py # To create/populate database and encrypt credentials
  python nurali_altair_task1_sever.py  # To run multi client TCP server
  python nurali_altair_task1_client.py  # To run TCP server
  ```




