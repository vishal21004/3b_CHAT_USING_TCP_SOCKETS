## reg no : 212222230177
## name : VISHAL M.A
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
CLIENT

```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

SERVER
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

## CLIENT:
![clnt 2](https://github.com/vishal21004/3b_CHAT_USING_TCP_SOCKETS/assets/119560110/0b05d5aa-073b-4a95-b690-96ae3e99b354)


## SERVER:
![srvr 2](https://github.com/vishal21004/3b_CHAT_USING_TCP_SOCKETS/assets/119560110/c9eb4ca5-ece9-4d5a-a165-f47349d00a36)











## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
