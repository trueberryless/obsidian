# What is Docker?

Docker is a platform for building, running, and shipping applications.

## Consistency

It allows you to package software versions and dependencies into a [[package]]. This package can then be reused by anyone, anywhere on any computer.

If you want to use this [[package]], you can simply compose it and run a [[container]]:

```
docker-compose up
```

Moreover, this method allows you to run different versions of the same dependency on one machine at the same time.
For example, you could run Node 9 and Node 14 simultaneously!

Additionally, you can remove all depencencies from your computer if the project is finished, by using:

```
docker-compose down --rmi all
```

# Virtual Machine vs Container

| Virtual Machine 	     | Container 	              |
|:---------------:       |:-----------:            	  |
| heavyweight      	     | lightweight 	              |
| own Operatimg System   | multiple apps in isolation |
| intensive resources    | less hardware resources    |

## Container

A container is an isolated environment for running an application.

- allow running multiple apps in isolation
- are lightweight
- use Operating System of the host
- start quickly
- need less hardware resources


## Virtual Machine

A virtual machine is an abstraction of a machine (physical hardware).

![[virtual_machine_2.png]]

### Hypervisors

These are examples for available hypervisors:

- VirtualBox
- VMware
- Hyper-V (Windows-only)

![[virtual_machine.png]]

### Problems

- each Virtual Machine needs a full-blown Operating System
- Virutal Machines are slow to start
- Virtual Machines need intensive resources

# Docker Architecture

Docker uses a Client-Server-Architecuture. So it has a Client component that talks to a server component using a REST API. The server - also called Docker engine - sits on the background and takes care of building and running containers.

![[docker_architecture.png]]

A container is technically a process like other processes on the computer. A process is a programm currently running / in action. All containers of the host share the Operating System - or more accurate: the kernel - of the host. A kernel manages applications and hardware resources (like memory and CPU).

![[docker_container.png]]

Every operating system has its own kernel and these kernels have different APIs. Hence, it is not possible to run a Windows application on Linux.

MacOS has its own kernel which native doesn't support docker [[container|continuous applications]]. In order to use docker on MacOS, you have to use a lightweight Linux Virtual Machine.

![[docker_architecture_2.png]]

