# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM:
### CLIENT: 
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
print(s.getsockname()) 
print(s.recv(1024).decode()) 
s.send("acknowledgement recived from the server".encode())
```
### SERVER:  
```
 import socket
 from datetime import datetime
 
s=socket.socket()
 
s.bind(('localhost',8000))
 
s.listen(5)
 c,addr=s.accept()
 print("Client Address : ",addr)
 
now = datetime.now()
 
c.send(now.strftime("%d/%m/%Y %H:%M:%S").encode()
```
## OUTPUT:
![Screenshot 2024-05-16 134330](https://github.com/Tanessha/2a_Stop_and_Wait_Protocol/assets/140876194/e1c4b372-e96f-4056-b846-3cffe2f23e47)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
