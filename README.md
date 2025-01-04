# Simple HTTP Web Server

This project is a basic HTTP web server implemented in Python using the `socket` module. It listens for incoming HTTP GET requests, serves requested files if they exist, and returns a 404 error for non-existent files.

---

## Features

- **HTTP Protocol Support**: Handles basic HTTP GET requests.
- **File Serving**: Serves files from the server's working directory.
- **Error Handling**: Returns a `404 Not Found` response for unavailable files.

---

## How It Works

1. **Socket Setup**:
   - The server binds to a specified port (`6789`) and listens for incoming TCP connections.
   
2. **Request Handling**:
   - Upon receiving a connection, the server processes the HTTP GET request.
   - The server attempts to locate the requested file in the current directory.

3. **Response**:
   - **File Found**: Sends a `200 OK` header followed by the file contents.
   - **File Not Found**: Sends a `404 Not Found` header and an HTML error message.

4. **Connection Closing**:
   - After serving the response, the server closes the client connection.

---

## Getting Started

### Prerequisites

- Python 3.x installed on your machine.

### Running the Server

1. Clone or download the repository.
2. Navigate to the directory containing the script.
3. Run the server:
   ```bash
   python3 webserver.py
