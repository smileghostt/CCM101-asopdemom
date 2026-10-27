# Mission Overview
The following mission involves handling server security. Using Uncomplicated Firewall (UFW), traffic must be blocked while allowing legitimate users to access the application freely.

# Objectives
The following are the objectives of the laboratory activity:
- Understanding concepts such as Attack Surface and Principle of Least Privelege (PoLP).
- Performing basic security audits on network ports within a Linux server.
- Configuration of UFW with a Default Deny policy.
- Implemetation of granular port management to allow SSH and HTTP traffic.
- Documentation of firewall rules and practices using Markdown.

# Commands Executed
- `docker run` - runs a container. If the container doesn't exist, pulls an image and creates a container.
- `curl` - used to transfer data from a server.
- `sudo` - super user do.
- `ufw allow ssh` - allows SSH connections to access the server. SSH can be replaced with ports to allow access to ports.
- `ufw default deny` - sets specific connection types to be denied by default. Can be specified as incoming or outgoing for example.
- `ufw default allow` - sets specific connection types to be allowed by default. Can be specified as well.
- `ufw enable` - enables the firewall.
- `ufw status` - checks the status of the firewall.

# Skills Learned
The skills that were learned were mostly centered towards firewall handling. Knowing how the firewall works allows for a start to properly secure your server. Utilizing this skill, you can set up proper security measures within servers that may be handled.
