# Palindrome Checker - Server-Client Application

## Overview
This project is a **server-client palindrome checker** implemented using **Python** and **socket programming**. The application consists of a **server** that processes palindrome requests and a **client** with a **Graphical User Interface (GUI)** to interact with the user.

The program supports:
- **Simple Palindrome Check**: Determines if a given string is a palindrome while ignoring spaces, punctuation, and case sensitivity.
- **Complex Palindrome Check**: Determines if a string can be rearranged to form a palindrome and calculates the minimum number of swaps required.

## Assignment Objective
The goal of this assignment is to develop a **concurrent server-client application** using **socket programming** that performs palindrome checking and allows multiple clients to connect simultaneously.

### Key Features:
- Multithreaded TCP Server to handle multiple client requests.
- Logging Mechanism to track client requests and responses.
- GUI Client using Tkinter for an interactive user experience.
- Timeout Handling: The client retries if the server does not respond within a given timeframe.
- Two modes of palindrome checking (simple and complex).

## Project Structure
```
├── server.py         # The server-side code handling palindrome checks
├── client.py         # The command-line based client (alternative to GUI)
├── gui.py            # The Tkinter-based GUI client
├── README.md         # This file containing project details
├── server_log.txt    # Log file recording client requests
```

## Installation and Execution
### Prerequisites
- Python 3.x

### Steps to Run the Program
#### 1. Start the Server
```sh
python server.py
```
This will start the TCP server, listening for client connections.

#### 2. Run the GUI Client
```sh
python gui.py
```
This will launch the graphical user interface where you can input a string and check for palindromes.

## How It Works
### Server
1. Receives client requests over a TCP connection.
2. Processes the request to check for palindrome properties.
3. Logs client interactions into `server_log.txt`.
4. Responds to the client with the palindrome check results.

### Client (GUI)
1. User inputs a string into the text box.
2. Selects Simple or Complex Palindrome Check using radio buttons.
3. Clicks 'Check', which sends the request to the server.
4. Receives and displays results in a message box.

## Example Usage
### Simple Palindrome Check
**Input:**
```
A man, a plan, a canal, Panama
```
**Processed as:**
```
amanaplanacanalpanama
```
**Output:**
```
Palindrome: True
```

### Complex Palindrome Check
**Input:**
```
ivicc
```
**Output:**
```
Palindrome: True
Swaps Needed: 2
```

## Additional Features
- **Logging**: The server logs each request with the client’s IP address, request type, input string, and result.
- **Timeout Handling**: The client will retry the request up to 3 times if the server does not respond.
- **GUI Enhancements**: A user-friendly graphical interface for ease of use.

## Conclusion
This project successfully implements a **networked palindrome checker** using Python's socket programming and Tkinter for the client GUI. The program handles **multiple clients**, maintains logs, and processes **both simple and complex palindrome checks** efficiently.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Author
Developed by **Your Name**
