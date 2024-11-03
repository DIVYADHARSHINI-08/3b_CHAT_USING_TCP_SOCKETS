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
## CLIENT :
```
Developed by: DIVYA DHARSHINI R
Reg no: 212223040042
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 
```
## SERVER :
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
![WhatsApp Image 2024-11-03 at 14 33 01_c7af3dc8](https://github.com/user-attachments/assets/4eaa192b-d83d-4a4a-92b9-b232f24daf86)

![WhatsApp Image 2024-11-03 at 14 33 02_daf548a8](https://github.com/user-attachments/assets/5582ccad-77bb-45c3-8c2c-f853357cf733)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
