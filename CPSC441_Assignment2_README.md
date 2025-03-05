# Proxy Server with Meme Injection

## Author
Created by Labib Ahmed

## Overview
This project implements an HTTP proxy server that intercepts client requests, forwards them to the destination server, and returns the response to the client. Additionally, it features an "Easter Egg" function and a meme injection mechanism that occasionally replaces images with random memes from a local folder.

## Features
- Acts as an HTTP proxy, forwarding client requests to the target server.
- Intercepts image responses and randomly replaces some with local meme images.
- Returns a meme image when a specific Easter Egg URL is accessed (`http://google.ca`).
- Handles multiple clients using multithreading.
- Graceful shutdown by pressing Enter.

## Folder Structure
```
project_folder/
│── memes/          # Folder containing meme images (jpg, png, gif)
│── proxy.py        # Main proxy server script
│── README.md       # Project documentation
```

## Requirements
- Python 3.x
- Required Python modules:
  - `socket`
  - `threading`
  - `re`
  - `random`
  - `os`
  - `base64`

## Installation
1. Clone or download this repository.
2. Install Python 3 if not already installed.
3. Ensure the `memes/` directory exists and contains some image files (`.jpg`, `.png`, `.gif`).
4. Run the script using:
   ```bash
   python proxy.py
   ```

## Configuration
The following configurations are defined at the beginning of the script:
- `PROXY_HOST = '127.0.0.1'`  (Localhost proxy server)
- `PROXY_PORT = 8080` (Port on which the proxy runs)
- `MEME_FOLDER = "./memes"` (Folder containing meme images)
- `EASTER_EGG_URL = "http://google.ca"` (Accessing this URL triggers an Easter Egg)
- `BUFFER_SIZE = 4096` (Defines data transfer chunk size)

## How It Works
1. The proxy listens for incoming client connections on `127.0.0.1:8080`.
2. When a client request is received:
   - It extracts the requested URL and host information.
   - If the request is for `http://google.ca`, it returns a random meme.
   - Otherwise, it forwards the request to the actual server.
3. The proxy checks if the response contains an image:
   - With a 10% probability, it replaces the image with a random meme.
   - Otherwise, it forwards the original image.

## Usage
1. Run the proxy server:
   ```bash
   python proxy.py
   ```
2. Configure your browser or applications to use the proxy:
   - HTTP Proxy: `127.0.0.1`
   - Port: `8080`
3. Browse normally, and enjoy random meme injections!
4. To shut down the server, press `Enter` in the terminal.

## Notes
- Only HTTP traffic is supported (HTTPS is not handled).
- If no memes are found in the `memes/` directory, image replacements will not occur.
- The script does not handle large file transfers efficiently and is meant for demonstration purposes.





