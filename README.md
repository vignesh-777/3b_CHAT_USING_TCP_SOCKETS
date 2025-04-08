# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM

#### server.py
```py
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```
#### client.py
```py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```

## OUPUT
#### server
![Screenshot 2025-04-08 113032](https://github.com/user-attachments/assets/30bd536d-da65-45b6-a98d-80bbb776112d)

#### client
![Screenshot 2025-04-08 113048](https://github.com/user-attachments/assets/3f3865cb-fd83-4c0a-a5df-a58d37678199)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
