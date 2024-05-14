# 2b IMPLEMENTATION OF SLIDING WINDOW PROTOCOL

 TARANIKKA A

 212223220115
 
 B.Tech IT
 
## AIM
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
## CLIENT:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept() 
size=int(input("Enter number of frames to send: "))
l=list(range(size))
s=int(input("Enter Window size:"))
st=0
i=0
```

## SERVER:
```
while True:
 while(i<len(l)):
    st+=s
        c.send(str(l[i:st]).encode())
        ack=c.recv(1024).decode()
        if ack:
        print(ack)
            i+=s
```
## OUPUT
### CLIENT:
![Screenshot 2024-02-27 142639](https://github.com/aswethaashok/2b_SLIDING_WINDOW_PROTOCOL/assets/149987410/4f8f00a5-56e7-40b1-ac5d-084f6f48e467)

### SERVER:
![Screenshot 2024-02-27 142701](https://github.com/aswethaashok/2b_SLIDING_WINDOW_PROTOCOL/assets/149987410/bbbed0c0-5c7a-44d4-aef8-8e5a37250d50)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed
