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
Client.py:


```
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

```

Server.py:

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



## OUPUT
Client.py:

![Screenshot 2024-04-29 142848](https://github.com/ZafreenJagir/3b_CHAT_USING_TCP_SOCKETS/assets/144870573/76853772-e7ab-4784-9b7a-b8d95ea2f66f)



Server.py



![Screenshot 2024-04-29 142856](https://github.com/ZafreenJagir/3b_CHAT_USING_TCP_SOCKETS/assets/144870573/26039c7d-6ba8-48f6-9ab2-fc75f351f31b)




## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
