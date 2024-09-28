# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## NAME : E.Mythri
## REG.NO : 212223240034
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
## Client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client>")
 s.send(msg.encode())
 print("Server>",s.recv(1024).decode())
```
## Server
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
  ClientMessage=c.recv(1024).decode()
  c.send(ClientMessage.encode())
```
## OUTPUT
## Client
![Screenshot 2024-09-26 113238](https://github.com/user-attachments/assets/e32b78be-1241-4fd3-83ac-7eeb98057446)

## Server
![Screenshot 2024-09-26 113330](https://github.com/user-attachments/assets/31c3ce45-4daf-4d85-890c-adfc23122e4b)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
