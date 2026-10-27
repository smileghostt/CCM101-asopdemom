# Technical Documentation
The following information is documentation of the commands used within the mission. These commands were used to secure the Nginx server and allow for a firewall to be set up for the server.

# Command used to allow SSH
> ### sudo allow ssh
> IMPORTANT COMMAND. This command allows for SSH connections to happen. It ensures that sudo commands and more after gaining a connection with the server is possible.

# Commands to set the Default Deny Policy
> ### sudo ufw default deny incoming
> This command blocks all incoming network connnections and traffic unless explicitly allowed.

> ### sudo ufw default allow outgoing
> The following command allows all outgoing network traffic and such to be permitted to leave the server.

# Command to allow Port 8080
> ### sudo ufw allow 8080/tcp
> This command allows port 8080 to be accessed externally using TCP. This can be applied to other ports if used.

# DISCLAIMER ⚠️
Running `sudo ufw enable` before running `sudo ufw allow ssh` will **PERMANENTLY** lock you out of the server. 