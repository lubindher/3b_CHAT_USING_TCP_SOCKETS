# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
## CLIENT:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## SERVER:
```
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
## OUPUT:
## CLIENT:
![Screenshot 2024-04-11 163504](https://github.com/23002027/3b_CHAT_USING_TCP_SOCKETS/assets/139752981/85f96000-e704-48cb-b74b-030137173d86)
## SERVER:
![Screenshot 2024-04-11 163515](https://github.com/23002027/3b_CHAT_USING_TCP_SOCKETS/assets/139752981/7d1d836f-f2c1-41f0-b9c9-24bcae5d2a5b)



## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
