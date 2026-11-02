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

# Server

```

import socket

s = socket.socket()
s.bind(('localhost', 8000))
s.listen(5)
c, addr = s.accept()

while True:
    msg = input("Enter a data: ")
    c.send(msg.encode())
    print(c.recv(1024).decode())


```



# Client 

```
import socket

s = socket.socket()
s.connect(('localhost', 8000))

while True:
    msg = s.recv(1024).decode()
    print(msg)
    s.send("Acknowledgement Recived".encode())

```



## OUTPUT
<img width="620" height="160" alt="image" src="https://github.com/user-attachments/assets/c7dcc997-4015-4502-bf33-fea895d55841" />

<img width="608" height="145" alt="image" src="https://github.com/user-attachments/assets/d719168d-53ce-4829-b968-63aaeb86569b" />


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed. 
