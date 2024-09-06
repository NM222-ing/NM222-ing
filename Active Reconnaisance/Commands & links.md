# Wappalyzer
> Browser extension for getting more information about the visited webpage (technologies used, technology version, etc.).

# ping
> Linux: ```ping -c 10 10.10.107.37```, Windows: ```ping -n 10 10.10.107.37``` -> specifying the number of pings (10 here).

# traceroute
> Linux: ```traceroute 10.10.107.37```. Getting the routes (nodes) from your machine to the target machine. Can change as the routing might be dynamic. On Linux TTL (Time To Live) is being sent 1st as TTL=1 -> it reaches the 1st node then comes back with TTL error -> then sends the next packet with TTL=2 and so on until it reached the destination.
> Windows: ```tracert 10.10.107.37```. On Windows, the TTL is set from the beginning -> it decreases with each node -> if it reached 0 but didn't arrive at the target host it returns TTL error and that's it.

# telnet
> Default port: 23. USing cleartext -> should use a secure alternative instead: SSH (Secure SHell). Can be used to collect the server banner.
> ```telnet 10.10.107.37 80``` then make a request: ```GET / HTTP/1.1```, then specify a host: ```host: example```, then an empty row -> you'll get more info about a specific webserver (basically you'll get a response from the server, like a GET request) -> can get Server Name and Version (like Apache 2.4.61, etc.).

# netcat
> For banner grabbing: ```nc 10.10.107.37 80``` followed by ```GET / HTTP/1.1``` and host, like telnet.
> ```nc -vnlp 1234``` open a port and listen for it on a specific path from a server. For client side: ```nc server_ip 1234```.
> Parameters: ```-l``` = Listen mode. ```-p``` = Specify the Port number (should appear just before the port number you want to listen on). ```-n``` = Numeric only; no resolution of hostnames via DNS (will avoid DNS lookups and warnings). ```-v``` = Verbose output (optional, yet useful to discover any bugs). ```-vv``` = Very Verbose (optional). ```-k``` = Keep listening after client disconnects.
> Port numbers less than 1024 require root privileges to listen on.
