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

## Special Features 

### Password Encryption
- The BCrypt Algorithm is used to hash and salt passwords in a secure way. BCrypt enables the creation of a password protection layer that can develop local hardware innovation in order to protect against long-term hazards or threats, such as attackers having the computational capacity to guess passwords twice as efficiently.

#### How bcrypt works?

![image](https://github.com/user-attachments/assets/ac355c5f-28bb-4db4-bc03-41a5d7000ec9)

- The BCrypt Algorithm was used in the db_population.py to encode values of credentials dictionary
- 
![image](https://github.com/user-attachments/assets/75191ad6-5a78-4b65-8292-b8125ce3d316)

#### Result of population

![image](https://github.com/user-attachments/assets/d1a32943-0dff-4eb1-a383-f78e68ddacf6)

### Authentication 
To verify a user's credentials by checking their username and password against stored values in an SQLite database.

![image](https://github.com/user-attachments/assets/e8cb0c9d-2d28-4f39-97f6-84b74374742f)

#### Algorithm
- Connect to Database
- Retrieve Stored Password Hash:
- Close Database Connection:
- Verify the Password
    If a result exists (i.e., the username is found in the database), extract the stored password hash.
    Convert the stored hash from a string to bytes (result[0].encode()).
    Compare the provided password (converted to bytes) with the stored hash using checkpw() (likely from the bcrypt library).
- Return Authentication Status
