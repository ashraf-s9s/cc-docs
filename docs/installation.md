There are several ways to get ClusterControl installed in your infrastructure. ClusterControl will be installed automatically if you deploy your database cluster using one of following ways:

* Severalnines Configurator (deployment package generated from severalnines.com/configurator for new database cluster deployment)
* Bootstrap script

It is advisable to setup package repository.

# Package Repository

Severalnines provides yum/apt package repository for ClusterControl packages. The repo is found at [http://repo.severalnines.com](http://repo.severalnines.com), with instructions provided on the landing page.

###Redhat/CentOS

1) Manually import the Severalnines repository public key into your RPM keyring:
```bash
$ rpm --import http://repo.severalnines.com/severalnines-repos.asc
```

2) Download the repository definition from our Severalnines download page:
```bash
$ wget http://www.severalnines.com/downloads/cmon/s9s-repo.repo -P /etc/yum.repos.d/
```

3) Look for ClusterControl packages:
```bash
$ yum search clustercontrol
```

###Debian/Ubuntu

1) Manually add Severalnines repository public key into your APT keyring:
```bash
$ wget http://repo.severalnines.com/severalnines-repos.asc -O- | sudo apt-key add -
```

2) Download the repository definition from our Severalnines download page:
```bash
$ sudo wget http://www.severalnines.com/downloads/cmon/s9s-repo.list -P /etc/apt/sources.list.d/
```

3) Update package list:
```bash
$ sudo apt-get update
```

4) Look for ClusterControl packages:
```bash
$ sudo apt-cache search clustercontrol
```

> *Omit 'sudo' if you are running as root.*

# Online Installation

Online installation requires internet connectivity on the ClusterControl node.

1) Install ClusterControl:

$ yum install clustercontrol clustercontrol-cmonapi clustercontrol-controller

2) Configure CMON with minimal options. Create a as follow:


3) Start the


ClusterControl UI is installed on /var/www/html/clustercontrol while ClusterControl REST API is installed on /var/www/html/cmonapi. At this stage, ClusterControl controller is yet to be installed by the post-installation script


# Offline Installation

**Redhat/CentOS**

Download

# Debian/Ubuntu

Download

