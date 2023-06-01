# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

### DATE:15-03-2023

### AIM :
To write a python program to perform stop and wait protocol

### ALGORITHM :
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client otherwise it will sendNACK
signal to client.
6. Stop the program.

### PROGRAM :
### CLIENT :
```
# Developed by : GOwrisankar.p
# Register Number : 212222230041
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
i=input("Enter a data: ")
c.send(i.encode())
ack=c.recv(1024).decode()
if ack:
print(ack)
continue
else:
c.close()
break
```
### Server:
```
# Developed by : S.JAIGANESH
# Register Number : 212222240037
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
print(s.recv(1024).decode())
s.send("Acknowledgement Received".encode())
```
### OUTPUT :
### CLient:
![Screenshot (25)](https://github.com/gowrisankarponnusamy/EX-2/assets/119393123/7fdfafba-c671-4eeb-978d-bd6e15fa31d8)
### Server:
![image](https://github.com/gowrisankarponnusamy/EX-2/assets/119393123/02b908ee-368a-441e-a02e-7e3031e4884d)

### RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.


