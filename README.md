# Class IS631 Spring 2019

## I create this repo to be use for the class IS631.

### No more install virtual machines, get into permission issues.

#### Follow the steps to get up and running with MS SQL Server
#### To get this you first need to install docker if you have Homebrew installed this should be easy, if nit just run this command:

```bash
$ brew cask install docker
```
check your installation you will see something similar

```bash
$ docker info

Containers: 3
 Running: 0
 Paused: 0
 Stopped: 3
Images: 25
Server Version: 18.09.1
Storage Driver: overlay2
 Backing Filesystem: extfs
 Supports d_type: true
 Native Overlay Diff: true
Logging Driver: json-file
Cgroup Driver: cgroupfs
Plugins:
 Volume: local
 Network: bridge host ipvlan macvlan null overlay
 Log: awslogs fluentd gcplogs gelf journald json-file local logentries splunk syslog
Swarm: inactive
Runtimes: runc
Default Runtime: runc
Init Binary: docker-init
containerd version: 9754871865f7fe2f4e74d43e2fc7ccd237edcbce
runc version: 96ec2177ae841256168fcf76954f7177af9446eb
init version: fec3683
Security Options:
 seccomp
  Profile: default
Kernel Version: 4.9.125-linuxkit
Operating System: Docker for Mac
OSType: linux
Architecture: x86_64
CPUs: 4
Total Memory: 1.952GiB
Name: linuxkit-025000000001
ID: BK3O:B7ZW:HHHE:EONZ:IZ5B:SNCC:74MG:BGLN:ONWD:FQ5E:WWWP:NZYX
Docker Root Dir: /var/lib/docker
Debug Mode (client): false
Debug Mode (server): true
 File Descriptors: 26
 Goroutines: 53
 System Time: 2019-01-31T02:52:29.2139293Z
 EventsListeners: 2
HTTP Proxy: gateway.docker.internal:3128
HTTPS Proxy: gateway.docker.internal:3129
Registry: https://index.docker.io/v1/
Labels:
Experimental: true
Insecure Registries:
 127.0.0.0/8
Live Restore Enabled: false
Product License: Community Engine

```
## Ready to proceed


### Step 1

clone this repo
```bash
$ git clone https://github.com/dguardia/MSSQL-IS631-2019.git
```

### Step 2
cd to the folder

```bash
$ cd is631-mssqlserver

```
### Step 3

```bash
$ docker-compose up -d
```

If you are not familiar with docker what we doing here is to start the service inside the containers in dettached mode lets try docker-compose

```bash
$ docker-compose

Define and run multi-container applications with Docker.

Usage:
  docker-compose [-f <arg>...] [options] [COMMAND] [ARGS...]
  docker-compose -h|--help

Options:
  -f, --file FILE             Specify an alternate compose file
                              (default: docker-compose.yml)
  -p, --project-name NAME     Specify an alternate project name
                              (default: directory name)

......................................... more code...............
```

Now the MS SQL server is up and running

### Optional

**For MAC Users: you can use terminal for mssql
```bash
$ npm install -g sql-cli
```
if doesn't work use `sudo`


### Step 4
To manage the database we will be using Azure Data Studio (Mac OX)

Use brew to do that

```bash
$ brew cask install azure-data-studio
```
### Step 5
Connect
Open the program it should be inside the application folder
or Cmd + space then the name "Azure Data Studio"

server: localhost
user: sa
password: Test@123 (same as line 12 docker-compose.yml)

### Done

I hope this will help to use it in class.

cheers!