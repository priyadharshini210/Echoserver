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
## Name: Priyadharshini P 
## Register No: 212223240128
## Server.py
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
## Client.py
```
import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Priyadharshini P (212223240128)")
    data = s.recv(1024)


print(f"Received {data!r}")
```
            

## OUTPUT:
## Server.py
![image](https://github.com/user-attachments/assets/cf00c8cb-90ce-4df2-9e58-de00eb0ec05b)
## Client.py
![image](https://github.com/user-attachments/assets/f34ff378-b662-4f38-a436-8355b54b9446)



## RESULT:
The program is executed successfully
