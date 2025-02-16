## Networking and Security

### Blocking all incoming traffic except SSH and HTTP.
First, the firewall needs to be turned on which was done with the command "sudo ufw enable". ufw means uncomplicated firewall.
Then all the incoming traffics were denied with the command "sudo ufw default deny incoming".
The incoming traffic from SSH and HTTP were given access with the folowing commands "sudo ufw allow 22/tcp" for SSH and "sudo ufw allow 80/tcp" for HTTP.
To verify if the changes took effect, the command "sudo ufw status verbose" was used.

### Checking which ports are currently open on the system.
To check the open ports, the command netstat with -tulnp options was used "sudo netstat -tulnp" netstat is used to display network connections, routing tables, interface statistics, and open ports the meanin of the options are -t to Show TCP ports, -u to Show UDP ports, -l to Show listening ports, -n to Show port numbers instead of service names and -p → Show which process is using each port.










