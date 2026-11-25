# 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME: M AADHAVAN NAGARAJAN
## REGISTER NUMBER: 212225040001
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
SERVER PROGARM:
```
import socket
s=socket.socket()
s.bind(('localhost',9999))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client> ", ClientMessage)
    msg=input("Server> ")
    c.send(msg.encode())
```
CLIENT PROGRAM:
```
import socket
s=socket.socket()
s.connect(('localhost', 9999))
while True:
    msg=input("Client> ")
    s.send(msg.encode())
    print("Server> ", s.recv(1024).decode())
```
## OUPUT
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6546740b-b440-4a50-94bc-c56b78660da2" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cf87f25a-253b-44b7-82e8-6234a20a245b" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
