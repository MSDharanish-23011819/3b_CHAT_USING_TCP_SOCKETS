## 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME : DHARANISH MS
## REGISTER NO : 212223240027

# AIM
To write a python program for creating Chat using TCP Sockets Links.
# ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
#  PROGRAM
## CLIENT 
```
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
# OUTPUT
## CLIENT

![3B CLIENT](https://github.com/MSDharanish-23011819/3b_CHAT_USING_TCP_SOCKETS/assets/147139454/fefde6e3-e8f9-46da-8248-fef59e745ce1)



## SERVER

![3B SERVER](https://github.com/MSDharanish-23011819/3b_CHAT_USING_TCP_SOCKETS/assets/147139454/9208afc0-3289-40fd-9559-2ad81a4d374a)

# RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
