# Containers

## Basics

Isola Recursos para um determinado fim (App/FileSystem/Users/Network/PIDs(processos))!

Cgroups: Modulo do Kernel Linux para Isolamento de CPU, Memória e Disco/IO(Inputs/Outputs).

Namespaces: Modulo do Kernel Linux - Isolamento de FileSystem, PIDs(processos), Network, Users e outros recursos.

Containers Hoje = something equal to a Modern Chroot (initially made to isolate resources)

Other examples:
- LXC: Solaris Zones
- Jails: FreeBSD
- VPS: OpenVZ (Negative for Performance: patches no Kernel Linux)
- 

Lista processos no Linux: ps -ef

Para instalar uma VM Ubuntu rapidamente no MacOs
```
brew install --cask multipass
multipass launch
multipass shell <instance_name>
```

Comando para installar utilitários do Cgroup: 
```
apt-get install cgroup-tools
```

Verificar comando Cgcreate
```
cgcreate -help
```

Criar grupos de controllers
```
cgcreate -g cpu,memory,blkdevices,freezer:giropops
ls /sys/fs/cgroup/cpu/giropops
```