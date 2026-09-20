## Comparison: Virtualization VS Containers
| Category            | Virtual Machines | Containers |
| ------------------- | :----------------: | :----------: |
| Architecture        |Virtual machines are Guest OSes built on a hypervisor|Containers are part of the Shared Host OS|
| Boot Time           |Virtual machines take minutes to boot considering it requres the entire OS|Containers take seconds to start up since it is isolated|
| Resource Efficiency |Heavy/High RAM needed, mostly because VMs are another OS|Lightweight/Low RAM, only need dependencies and is isolated to just what is needed|
| Isolation Level     |Hardware-level, considering the hypervisor|Process-level, provided by the OS kernel features|

## Why would you consider moving from VMs to Containers?
As presented within the table, VMs, depending on what may be used, can be excessive for its purpose. When a VM is merely used for one specific purpose, it might end up consuming more than what is worth. Containers on the other hand can be used to make your web applications faster as it only consumes necessary resources rather than require an entire OS to function.