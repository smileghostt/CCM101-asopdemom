The following is a manual made for the cloud architecture that is made.

# SSH
In order to SSH into the server, you must use the following credentials:
- use command `ssh vboxuser@[VM.LOCAL.IP]`
    - you can change the ip to your vm's own local ip depending on the network you used
- password: password123

It is highly recommended to do so the moment the Ubuntu Server is open. This provides full control, as the VM only exists to provide the service.

Remember that if you have transferred the VM to a different device, you may have to add these within your hosts (in windows, its in `System32/devices/etc/hosts`, be admin to modify) file in order to access the containers without needing to change your DNS:

- [VM.LOCAL.IP]  vault.cloudnova.server
- [VM.LOCAL.IP]  gitea.cloudnova.server
- [VM.LOCAL.IP]  pihole.cloudnova.server


The following architecture has these containers:
- Gitea
- Vaultwarden
- Pihole
- Nginx
- PostgreSQL

# Gitea
Gitea doesn't need as much maintaining. It is meant to provide an alternative to Github for development projects.

root account:
- rootaccount
- QWxxLUcwiJ4naH

test account:
- John_Doe
- testpassword

# Vaultwarden
If you need to make a new account on vaultwarden, you can set `SIGNUPS_ALLOWED` to true. However, for this setup, it is set to false to only allow the root account to store passwords. Vaultwarden allows for employees and personnels to store passwords and information.
- root@cloudnova.server
- newpassword-2_true

# Pihole
Pihole is a DNS sink that works both as an adblocker and a way to access the server in the first place through the server's custom DNS. This ensures that the server is not accessible through the public internet, and ensures that it only exists within the network.

- Password: newpassword-2_true

When the network is switched over to something else, you will have to change the DNS sink

# Main user account stuff
- cloudnova-admin
- newpassword-2_true