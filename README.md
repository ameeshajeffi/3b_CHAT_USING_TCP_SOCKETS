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
# Client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

# Server
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

![322514815-3b201be5-286e-4c0c-8850-196d6fc63d19](https://github.com/user-attachments/assets/08415ec4-0a38-4d0e-9ba4-29717e50903f)

![322514861-0adf18e4-39c9-47c3-ab12-b565672b312d](https://github.com/user-attachments/assets/f5a1d4af-02ed-4915-a37e-2da29c13790f)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
