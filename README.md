# Echoserver
Echo server and client using python socket

## AIM:
To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
### Server code:
echo-server.py
```py
import socket
host='121.0.0.1'
port=12345
server_socket=socket.socket(socket.AF_INET,socket.SOCK_STREAM)
server_socket.bind((host,port))
server_socket.listen(1)
print("Server listening on {}:{}".format(host,port))
client_socket,addr=server_socket.accept()
print("Connected to",addr)
data=client_socket.recv(1024).decode()
print("Received:",data)
response="Hello Client"
client_socket.send(response.encode())
client_socket.close
server_socket.close
```
### Client code:
echo-client.py
```py
import socket
host = '127.0.0.1' 
port = 12345 
client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
client_socket.connect((host, port))
message = 'Hello, server!'
client_socket.send(message.encode())
response = client_socket.recv(1024).decode()
print('Server response:', response)
# Close the connection
client_socket.close()
```

## OUTPUT:
### Server Output
![774a509d-003b-4d7d-abea-ad65f0b87484](https://github.com/Prajeeth17/Echoserver/assets/120513885/060d042b-cb45-490f-a708-2c1cd7b72526)
### Client Output
![1fc8d862-3dc2-42ce-baa7-2daa27add0a6](https://github.com/Prajeeth17/Echoserver/assets/120513885/0fe61cb8-9349-4944-885d-d58275a8780f)

## RESULT:
The program is executed successfully
