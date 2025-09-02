# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
NAME : PRATHIKSHA R REG NO : 212224040244
## Client :
```
# echo-client.py

import socket
HOST = "127.0.0.1"
PORT = 65432  
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, world")
    data = s.recv(1024)
print(f"Received {data!r}")
```
## Server:
```
# echo-server.py
import socket
HOST = "127.0.0.1"
PORT = 65432  
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
```
## OUTPUT
<img width="1028" height="71" alt="image" src="https://github.com/user-attachments/assets/f9b6b044-4624-461a-bb7a-be9e4c7c5269" />

## RESULT:
The program is executed successfully
