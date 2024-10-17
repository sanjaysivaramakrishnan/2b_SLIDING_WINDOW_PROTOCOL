# 2b IMPLEMENTATION OF SLIDING WINDOW PROTOCOL
## AIM
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
## OUPUT
## RESULT# 2b IMPLEMENTATION OF SLIDING WINDOW PROTOCOL
### Date:
## AIM:
To implement of slliding window protocol.
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
#### Develped by: Ramya R
#### Register number: 212223230169
## CLIENT
```
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
size=int(input("Enter number of frames to send : ")) 
l=list(range(size)) 
s=int(input("Enter Window Size : ")) 
st=0 
i=0 
while True: 
    while(i<len(l)): 
            st+=s 
            c.send(str(l[i:st]).encode()) 
            ack=c.recv(1024).decode() 
            if ack: 
                print(ack) 
                i+=s
```
## SERVER
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000))  
while True:    
    print(s.recv(1024).decode()) 
    s.send("acknowledgement recieved from the server".encode())
```


## OUTPUT
## CLIENT
![image](https://github.com/user-attachments/assets/78b494b9-34f2-4b70-8cfe-e42a7c90791c)

## SERVER
![image](https://github.com/user-attachments/assets/c880a390-39b0-4433-b3af-ec1f2cd8acb8)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed

Thus, python program to perform stop and wait protocol was successfully executed
