# Docker

### Docker provides All layers of provisioning tools.

#### Provisioning Tools

__Orchestration Layer (Application)__
- Process: Deploy applications, Set up applications, Register service, Monitor services
- Tool:Consul, Kubernetes(for Docker Container)

__Configuration Layer (Middleware)__
- Process: Install middrewares, Set up middrewares, Set up ini file(under /etc) & user
- Tool:Ansible, Chef

__Bootstrapping Layer (OS)__
- Process: Install OS,  Boot OS, Set up services & security of OS, Network configraion
- Tool: Vagrant, KickStart


#### Container
- Create logical section as a process using namespace on Host OS.
- Namespace is PID, Network, UID, Mount, UTS, IPC(that is shared memory & semaphore).
- Cgroup is used for sharing resources(memory, process, CPU).
- Each process & file system cannot access each other.
- Deploy Libraries, Applications. 
- Deploy light OS.(Not include Kernel.) 
- Use some functions of host OS.(To realize light resource load & fast process.)
- Docker is implemented by Go lang.
- High portablity.
- Docker image is just directory to execute a specific application.
- Network configration is Physical NIC(eh0)-Docker Bridge(docker0) - Virtual NIC(veth0x) - Container eth0.
- Link function is used for communicating between dockers.
- NAPT is used for communicating between docker and external network.
- NAPT(IP Masquerade) is transforming IP and Port using iptables.

__Create & Execute Docker images__
- Docker Engine

__Configure & Manage Dockers__
- Docker Compose: Configraion Management
- Docker Swarm: Clustering Management
- Docker Machine: Building Execution Environment

__Share Dockers__
- Docker Registry

