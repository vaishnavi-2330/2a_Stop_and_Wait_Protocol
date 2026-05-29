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
## PROGRAM
## SERVER:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
print(s.recv(1024).decode()) 
s.send("Acknowledgement Recived".encode())
```

## CLIENT:
```
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
i=input("Enter a data: ") 
c.send(i.encode()) 
Type your text 
ack=c.recv(1024).decode() 
if ack: 
print(ack) 
continue 
else: 
c.close() 
break
```

## OUTPUT:
<img width="1871" height="1002" alt="Screenshot 2026-05-20 181851" src="https://github.com/user-attachments/assets/0b5b3756-4657-4d10-abbc-2c820d01b62e" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
