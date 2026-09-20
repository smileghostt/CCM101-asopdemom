# Reflection 💭
Having completed the former checkpoints, enough information has been gathered to parse out answers to the questions given. Starting with the difference in boot time between virtual machines and Containers. The boot times within containers compared to a virtual machine are night and day. Within containers, boot times usually last around a few seconds before they are completed. Meanwhile, virtual machines may take minutes in order to properly boot due to hardware requirements and overhead. Depending on what is needed, you may need quicker boot times for more isolated applications.

Port mapping is a way to be able to expose network services within a Docker container. Port 8080:80, meanwhile, is a huge necessity to port forward to in order for the PC to be able to communicate with the network. The necessity for this is due to Docker containers being isolated, and forwarding to an open port allows you to be able to access the service.

Data inside a container will be permanently deleted if you were to remove the container. Simple as that. Without the container, any data stored within it gets completely wiped out.

As for how this would change the way developers and teams handle their work or work together, I believe that containerizing allows for separation of concerns to be cleanly handled. Each developer and/or team member can work on specific containers neatly. If one thing breaks, then deduction on what has been broken can easily be done.

Lastly, regarding my GitHub Portfolio. Mostly fine, I suppose nothing much can be said other than it is going rather smoothly. I'm unable to provide much since this is honestly how I think of it as of the moment.