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
Echo-Server:
```
import socket


HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)


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
Echo-Client:
```
import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello I am Rudesh kanna R  (212223233002)")
    data = s.recv(1024)


print(f"Received {data!r}")
```

## OUTPUT:
![Screenshot 2025-03-16 113542](https://github.com/user-attachments/assets/e3270ff7-8860-45dc-a579-aa09b041167f)
![Screenshot 2025-03-16 113520](https://github.com/user-attachments/assets/d7f37913-d24d-41a0-be80-c4536f4a6ca9)
![Screenshot 2025-03-16 113451](https://github.com/user-attachments/assets/27ad61b6-e623-4fd9-b928-b58145dbeab5)

## RESULT:
The program is executed successfully
