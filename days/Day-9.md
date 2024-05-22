# Learned
### Fundamentals of Python
   - Sockets
   - Building a Port Scanner

# A Few Details
### Sockets
```python
#SOCKETS - Sockets can be used to connect two nodes together.#!/bin/python3import socket

HOST = '127.0.0.1'
PORT = 7777

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)#af_inet is ipv4, sock stream is a port
s.connect((HOST,PORT))
```
### Building a Port Scanner
```python
#!/bin/python3import sys
import socket
from datetime import datetime

#Define our targetif len(sys.argv) == 2:
	target = socket.gethostbyname(sys.argv[1])#Translate hostname to IPv4else:
	print("Invalid amount of arguments.")
	print("Syntax: python3 scanner.py")

#Add a pretty banner
print("-" * 50)
print("Scanning target "+target)
print("Time started: "+str(datetime.now()))
print("-" * 50)

try:
	for port in range(50,85):
		s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
		socket.setdefaulttimeout(1)
		result = s.connect_ex((target,port))#returns an error indicator - if port is open it throws a 0, otherwise 1if result == 0:
			print("Port {} is open".format(port))
		s.close()

except KeyboardInterrupt:
	print("\nExiting program.")
	sys.exit()

except socket.gaierror:
	print("Hostname could not be resolved.")
	sys.exit()

except socket.error:
	print("Could not connect to server.")
	sys.exit()
```