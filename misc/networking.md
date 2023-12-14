# check all open ports of host

1. Nmap can use it to scan for open ports on a remote host.

nmap host

2. You can use the telnet command to check if a specific port is open on a host. This won't show you a list of all open ports, but it can help check individual ports.

telnet [hostname or IP] [port]

3. Using netstat locally:

On the host itself, you can use the netstat command to display a list of open ports.

netstat -an | grep LISTEN

4. You can also use a Python script to scan for open ports. Here's a simple example using the socket module:

import socket

def scan_ports(hostname, start_port, end_port):
for port in range(start_port, end_port + 1):
sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
sock.settimeout(1)
result = sock.connect_ex((hostname, port))
if result == 0:
print(f"Port {port} is open")
sock.close()

# Example usage

scan_ports("example.com", 1, 1000)
