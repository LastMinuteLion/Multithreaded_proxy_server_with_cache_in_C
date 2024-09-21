# Proxy Server with Cache

## Overview
This project implements a multi-threaded HTTP proxy server with caching capabilities. The server listens for client requests, forwards them to the appropriate remote server, and caches the responses to improve performance for subsequent requests.

For more information, visit [Eraser Workspace](https://app.eraser.io/workspace/Z0PC1gUS3qRn9oAB8mDI?origin=share).

## Features
- **Multi-threading**: Handles multiple client requests simultaneously using POSIX threads.
- **Caching**: Stores responses from remote servers to reduce latency for repeated requests.
- **Error Handling**: Sends appropriate HTTP error messages for various client request issues.
- **HTTP Version Support**: Supports both HTTP/1.0 and HTTP/1.1 protocols.

## Components
- **Cache Element Structure**: Defines the structure for cache elements, including data, URL, length, and last accessed time.
- **Request Handling**: Parses incoming requests, forwards them to the remote server, and manages responses.
- **Thread Management**: Uses semaphores and mutexes to manage concurrent access to shared resources.

## Dependencies
- POSIX threads (`pthread`)
- Standard C libraries (`stdio.h`, `stdlib.h`, `string.h`, etc.)
- Networking libraries (`sys/socket.h`, `netinet/in.h`, etc.)

## Usage
1. Compile the project using a C compiler (e.g., `gcc`).
2. Run the server with the desired port number:
   ```bash
   ./proxy_server_with_cache <port_number>
   ```
3. Configure your web browser or HTTP client to use the proxy server.

## Example
To run the server on port 8080:
```bash
./proxy_server_with_cache 8080
```

## Error Codes
- **400**: Bad Request
- **403**: Forbidden
- **404**: Not Found
- **500**: Internal Server Error
- **501**: Not Implemented
- **505**: HTTP Version Not Supported

## Contributing
Contributions are welcome! Please submit a pull request or open an issue for any enhancements or bug fixes. For more details, check the [Eraser Workspace](https://app.eraser.io/workspace/Z0PC1gUS3qRn9oAB8mDI?origin=share).

## License
This project is licensed under the MIT License.

---

Feel free to modify any sections to better fit your project's specifics or your personal preferences!