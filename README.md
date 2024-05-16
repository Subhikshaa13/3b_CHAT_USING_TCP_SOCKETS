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
Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
Server:
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
## OUPUT
![310591158-bfde4f04-8899-4eb5-b66e-2e476a44853d](https://github.com/Subhikshaa13/3b_CHAT_USING_TCP_SOCKETS/assets/118787344/f1f958cd-377e-4ecf-bac7-4214c1bf5ba7)
![310591403-342ff6fb-d9aa-4c94-a682-ac6df8c0af33](https://github.com/Subhikshaa13/3b_CHAT_USING_TCP_SOCKETS/assets/118787344/ad5dfbb6-e28f-480b-9b1c-c08d7a6c1df2)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
