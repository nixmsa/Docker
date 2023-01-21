<pre>
<h1> Docker Desktop </h1>
<b> Docker installation CLI </b>
root@u22dsktop:~# curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/docker-archive-keyring.gpg
File '/etc/apt/trusted.gpg.d/docker-archive-keyring.gpg' exists. Overwrite? (y/N) y
root@u22dsktop:~# ls -ltr
total 4
drwx------ 5 root root 4096 Jan 21 09:51 snap
root@u22dsktop:~# sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
Repository: 'deb [arch=amd64] https://download.docker.com/linux/ubuntu jammy stable'
Description:
Archive for codename: jammy components: stable
More info: https://download.docker.com/linux/ubuntu
Adding repository.
Press [ENTER] to continue or Ctrl-c to cancel.
Adding deb entry to /etc/apt/sources.list.d/archive_uri-https_download_docker_com_linux_ubuntu-jammy.list
Adding disabled deb-src entry to /etc/apt/sources.list.d/archive_uri-https_download_docker_com_linux_ubuntu-jammy.list
Get:1 https://download.docker.com/linux/ubuntu jammy InRelease [48.9 kB]
Hit:2 http://security.ubuntu.com/ubuntu jammy-security InRelease                                                                  
Hit:3 http://ca.archive.ubuntu.com/ubuntu jammy InRelease                                                 
Hit:4 http://ca.archive.ubuntu.com/ubuntu jammy-updates InRelease
Hit:5 http://ca.archive.ubuntu.com/ubuntu jammy-backports InRelease
Get:6 https://download.docker.com/linux/ubuntu jammy/stable amd64 Packages [11.9 kB]
Fetched 60.8 kB in 2s (28.9 kB/s)
Reading package lists... Done
root@u22dsktop:~#  apt install docker-ce docker-ce-cli containerd.io uidmap -y
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following package was automatically installed and is no longer required:
  systemd-hwe-hwdb
Use 'apt autoremove' to remove it.
The following additional packages will be installed:
  docker-ce-rootless-extras docker-scan-plugin git git-man liberror-perl libslirp0 pigz slirp4netns
Suggested packages:
  aufs-tools cgroupfs-mount | cgroup-lite git-daemon-run | git-daemon-sysvinit git-doc git-email git-gui gitk gitweb git-cvs
  git-mediawiki git-svn
The following NEW packages will be installed:
  containerd.io docker-ce docker-ce-cli docker-ce-rootless-extras docker-scan-plugin git git-man liberror-perl libslirp0 pigz
  slirp4netns uidmap
0 upgraded, 12 newly installed, 0 to remove and 249 not upgraded.
Need to get 107 MB of archives.
After this operation, 407 MB of additional disk space will be used.
Get:1 https://download.docker.com/linux/ubuntu jammy/stable amd64 containerd.io amd64 1.6.15-1 [27.7 MB]
Get:2 http://ca.archive.ubuntu.com/ubuntu jammy/universe amd64 pigz amd64 2.6-1 [63.6 kB]
Get:3 http://ca.archive.ubuntu.com/ubuntu jammy/main amd64 liberror-perl all 0.17029-1 [26.5 kB]
Get:4 http://ca.archive.ubuntu.com/ubuntu jammy-updates/main amd64 git-man all 1:2.34.1-1ubuntu1.6 [953 kB]
Get:5 http://ca.archive.ubuntu.com/ubuntu jammy-updates/main amd64 git amd64 1:2.34.1-1ubuntu1.6 [3,142 kB]
Get:6 https://download.docker.com/linux/ubuntu jammy/stable amd64 docker-ce-cli amd64 5:20.10.23~3-0~ubuntu-jammy [42.6 MB]
Get:7 http://ca.archive.ubuntu.com/ubuntu jammy/main amd64 libslirp0 amd64 4.6.1-1build1 [61.5 kB]                                
Get:8 http://ca.archive.ubuntu.com/ubuntu jammy/universe amd64 slirp4netns amd64 1.0.1-2 [28.2 kB]                                
Get:9 http://ca.archive.ubuntu.com/ubuntu jammy-updates/universe amd64 uidmap amd64 1:4.8.1-2ubuntu2.1 [22.4 kB]                  
Get:10 https://download.docker.com/linux/ubuntu jammy/stable amd64 docker-ce amd64 5:20.10.23~3-0~ubuntu-jammy [20.5 MB]          
Get:11 https://download.docker.com/linux/ubuntu jammy/stable amd64 docker-ce-rootless-extras amd64 5:20.10.23~3-0~ubuntu-jammy [8,390 kB]
Get:12 https://download.docker.com/linux/ubuntu jammy/stable amd64 docker-scan-plugin amd64 0.23.0~ubuntu-jammy [3,623 kB]        
Fetched 107 MB in 11s (9,644 kB/s)                                                                                                
Selecting previously unselected package pigz.
(Reading database ... 195601 files and directories currently installed.)
Preparing to unpack .../00-pigz_2.6-1_amd64.deb ...
Unpacking pigz (2.6-1) ...
Selecting previously unselected package containerd.io.
Preparing to unpack .../01-containerd.io_1.6.15-1_amd64.deb ...
Unpacking containerd.io (1.6.15-1) ...
Selecting previously unselected package docker-ce-cli.
Preparing to unpack .../02-docker-ce-cli_5%3a20.10.23~3-0~ubuntu-jammy_amd64.deb ...
Unpacking docker-ce-cli (5:20.10.23~3-0~ubuntu-jammy) ...
Selecting previously unselected package docker-ce.
Preparing to unpack .../03-docker-ce_5%3a20.10.23~3-0~ubuntu-jammy_amd64.deb ...
Unpacking docker-ce (5:20.10.23~3-0~ubuntu-jammy) ...
Selecting previously unselected package docker-ce-rootless-extras.
Preparing to unpack .../04-docker-ce-rootless-extras_5%3a20.10.23~3-0~ubuntu-jammy_amd64.deb ...
Unpacking docker-ce-rootless-extras (5:20.10.23~3-0~ubuntu-jammy) ...
Selecting previously unselected package docker-scan-plugin.
Preparing to unpack .../05-docker-scan-plugin_0.23.0~ubuntu-jammy_amd64.deb ...
Unpacking docker-scan-plugin (0.23.0~ubuntu-jammy) ...
Selecting previously unselected package liberror-perl.
Preparing to unpack .../06-liberror-perl_0.17029-1_all.deb ...
Unpacking liberror-perl (0.17029-1) ...
Selecting previously unselected package git-man.
Preparing to unpack .../07-git-man_1%3a2.34.1-1ubuntu1.6_all.deb ...
Unpacking git-man (1:2.34.1-1ubuntu1.6) ...
Selecting previously unselected package git.
Preparing to unpack .../08-git_1%3a2.34.1-1ubuntu1.6_amd64.deb ...
Unpacking git (1:2.34.1-1ubuntu1.6) ...
Selecting previously unselected package libslirp0:amd64.
Preparing to unpack .../09-libslirp0_4.6.1-1build1_amd64.deb ...
Unpacking libslirp0:amd64 (4.6.1-1build1) ...
Selecting previously unselected package slirp4netns.
Preparing to unpack .../10-slirp4netns_1.0.1-2_amd64.deb ...
Unpacking slirp4netns (1.0.1-2) ...
Selecting previously unselected package uidmap.
Preparing to unpack .../11-uidmap_1%3a4.8.1-2ubuntu2.1_amd64.deb ...
Unpacking uidmap (1:4.8.1-2ubuntu2.1) ...
Setting up docker-scan-plugin (0.23.0~ubuntu-jammy) ...
Setting up uidmap (1:4.8.1-2ubuntu2.1) ...
Setting up liberror-perl (0.17029-1) ...
Setting up containerd.io (1.6.15-1) ...
Created symlink /etc/systemd/system/multi-user.target.wants/containerd.service → /lib/systemd/system/containerd.service.
Setting up docker-ce-cli (5:20.10.23~3-0~ubuntu-jammy) ...
Setting up libslirp0:amd64 (4.6.1-1build1) ...
Setting up pigz (2.6-1) ...
Setting up git-man (1:2.34.1-1ubuntu1.6) ...
Setting up docker-ce-rootless-extras (5:20.10.23~3-0~ubuntu-jammy) ...
Setting up slirp4netns (1.0.1-2) ...
Setting up docker-ce (5:20.10.23~3-0~ubuntu-jammy) ...
Created symlink /etc/systemd/system/multi-user.target.wants/docker.service → /lib/systemd/system/docker.service.
Created symlink /etc/systemd/system/sockets.target.wants/docker.socket → /lib/systemd/system/docker.socket.
Setting up git (1:2.34.1-1ubuntu1.6) ...
Processing triggers for man-db (2.10.2-1) ...
Processing triggers for libc-bin (2.35-0ubuntu3.1) ...
root@u22dsktop:~# 
root@u22dsktop:~# exit
logout
There are stopped jobs.
root@u22dsktop:~# exit
logout
mahsan@u22dsktop:~$ sudo usermod -aG docker $USER
[sudo] password for mahsan: 
mahsan@u22dsktop:~$ newgrp docker
mahsan@u22dsktop:~$ id
uid=1000(mahsan) gid=999(docker) groups=999(docker),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),122(lpadmin),134(lxd),135(sambashare),1000(mahsan)
mahsan@u22dsktop:~$ ip addr
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host 
       valid_lft forever preferred_lft forever
2: ens33: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 00:0c:29:56:81:07 brd ff:ff:ff:ff:ff:ff
    altname enp2s1
    inet 192.168.18.131/24 brd 192.168.18.255 scope global dynamic noprefixroute ens33
       valid_lft 1495sec preferred_lft 1495sec
    inet6 fe80::147a:68f0:32b6:c9b9/64 scope link noprefixroute 
       valid_lft forever preferred_lft forever
3: docker0: <NO-CARRIER,BROADCAST,MULTICAST,UP> mtu 1500 qdisc noqueue state DOWN group default 
    link/ether 02:42:db:09:c7:8c brd ff:ff:ff:ff:ff:ff
    inet 172.17.0.1/16 brd 172.17.255.255 scope global docker0
       valid_lft forever preferred_lft forever
mahsan@u22dsktop:~$ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
mahsan@u22dsktop:~$ docker images
REPOSITORY   TAG       IMAGE ID   CREATED   SIZE
mahsan@u22dsktop:~$ systemctl status docker
● docker.service - Docker Application Container Engine
     Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
     Active: active (running) since Sat 2023-01-21 10:41:04 PST; 9min ago
TriggeredBy: ● docker.socket
       Docs: https://docs.docker.com
   Main PID: 17829 (dockerd)
      Tasks: 8
     Memory: 22.1M
        CPU: 886ms
     CGroup: /system.slice/docker.service
             └─17829 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock

Jan 21 10:41:03 u22dsktop dockerd[17829]: time="2023-01-21T10:41:03.828630562-08:00" level=info msg="scheme \"unix\" not registere>
Jan 21 10:41:03 u22dsktop dockerd[17829]: time="2023-01-21T10:41:03.828648088-08:00" level=info msg="ccResolverWrapper: sending up>
Jan 21 10:41:03 u22dsktop dockerd[17829]: time="2023-01-21T10:41:03.828656945-08:00" level=info msg="ClientConn switching balancer>
Jan 21 10:41:03 u22dsktop dockerd[17829]: time="2023-01-21T10:41:03.898067307-08:00" level=info msg="Loading containers: start."
Jan 21 10:41:04 u22dsktop dockerd[17829]: time="2023-01-21T10:41:04.326191978-08:00" level=info msg="Default bridge (docker0) is a>
Jan 21 10:41:04 u22dsktop dockerd[17829]: time="2023-01-21T10:41:04.661035339-08:00" level=info msg="Loading containers: done."
Jan 21 10:41:04 u22dsktop dockerd[17829]: time="2023-01-21T10:41:04.878639646-08:00" level=info msg="Docker daemon" commit=6051f14>
Jan 21 10:41:04 u22dsktop dockerd[17829]: time="2023-01-21T10:41:04.878832597-08:00" level=info msg="Daemon has completed initiali>
Jan 21 10:41:04 u22dsktop systemd[1]: Started Docker Application Container Engine.
Jan 21 10:41:04 u22dsktop dockerd[17829]: time="2023-01-21T10:41:04.984234946-08:00" level=info msg="API listen on /run/docker.soc>
mahsan@u22dsktop:~$ docker version
Client: Docker Engine - Community
 Version:           20.10.23
 API version:       1.41
 Go version:        go1.18.10
 Git commit:        7155243
 Built:             Thu Jan 19 17:45:08 2023
 OS/Arch:           linux/amd64
 Context:           default
 Experimental:      true

Server: Docker Engine - Community
 Engine:
  Version:          20.10.23
  API version:      1.41 (minimum version 1.12)
  Go version:       go1.18.10
  Git commit:       6051f14
  Built:            Thu Jan 19 17:42:57 2023
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.6.15
  GitCommit:        5b842e528e99d4d4c1686467debf2bd4b88ecd86
 runc:
  Version:          1.1.4
  GitCommit:        v1.1.4-0-g5fd4c4d
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
mahsan@u22dsktop:~$ wget https://desktop.docker.com/linux/main/amd64/docker-desktop-4.15.0-amd64.deb
--2023-01-21 10:50:56--  https://desktop.docker.com/linux/main/amd64/docker-desktop-4.15.0-amd64.deb
Resolving desktop.docker.com (desktop.docker.com)... 18.172.170.4, 18.172.170.28, 18.172.170.100, ...
Connecting to desktop.docker.com (desktop.docker.com)|18.172.170.4|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 490180928 (467M)
Saving to: ‘docker-desktop-4.15.0-amd64.deb’

docker-desktop-4.15.0-amd64.deb  100%[=========================================================>] 467.47M  10.1MB/s    in 59s     

2023-01-21 10:51:54 (7.98 MB/s) - ‘docker-desktop-4.15.0-amd64.deb’ saved [490180928/490180928]

***
ahsan@u22dsktop:~$ wget https://desktop.docker.com/linux/main/amd64/docker-desktop-4.15.0-amd64.deb
--2023-01-21 10:50:56--  https://desktop.docker.com/linux/main/amd64/docker-desktop-4.15.0-amd64.deb
Resolving desktop.docker.com (desktop.docker.com)... 18.172.170.4, 18.172.170.28, 18.172.170.100, ...
Connecting to desktop.docker.com (desktop.docker.com)|18.172.170.4|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 490180928 (467M)
Saving to: ‘docker-desktop-4.15.0-amd64.deb’

docker-desktop-4.15.0-amd64.deb  100%[=========================================================>] 467.47M  10.1MB/s    in 59s     

2023-01-21 10:51:54 (7.98 MB/s) - ‘docker-desktop-4.15.0-amd64.deb’ saved [490180928/490180928]

***

mahsan@u22dsktop:~$ sudo apt install ./docker-desktop-4.15.0-amd64.deb 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Note, selecting 'docker-desktop' instead of './docker-desktop-4.15.0-amd64.deb'
The following package was automatically installed and is no longer required:
  systemd-hwe-hwdb

ahsan@u22dsktop:~$ sudo apt install ./docker-desktop-4.15.0-amd64.deb 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Note, selecting 'docker-desktop' instead of './docker-desktop-4.15.0-amd64.deb'
docker-desktop is already the newest version (4.15.0-93002).
The following package was automatically installed and is no longer required:
  systemd-hwe-hwdb
Use 'sudo apt autoremove' to remove it.
0 upgraded, 0 newly installed, 0 to remove and 249 not upgraded.
mahsan@u22dsktop:~$

</pre>


## Docker ##
![Alt text](d1.png "Optional title")
![Alt text](d2.png "Optional title")
![Alt text](d3.png "Optional title")
![Alt text](d4.png "Optional title")
![Alt text](d5.png "Optional title")
![Alt text](d6.png "Optional title")
![Alt text](d7.png "Optional title")
![Alt text](d8.png "Optional title")
![Alt text](d9.png "Optional title")
![Alt text](d10.png "Optional title")
![Alt text](d11.png "Optional title") 
![Alt text](d12.png "Optional title")
![Alt text](d13.png "Optional title")
![Alt text](d14.png "Optional title")
![Alt text](d15.png "Optional title")
![Alt text](d16.png "Optional title")
![Alt text](d17.png "Optional title")
![Alt text](d18.png "Optional title")
![Alt text](d19.png "Optional title")
![Alt text](d20.png "Optional title")
![Alt text](d21.png "Optional title")
![Alt text](d22.png "Optional title")
![Alt text](d23.png "Optional title")
![Alt text](d24.png "Optional title")
![Alt text](d25.png "Optional title")
![Alt text](d26.png "Optional title")
![Alt text](d27.png "Optional title")

