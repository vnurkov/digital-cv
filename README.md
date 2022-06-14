# Education

- (2009-2013) Mechanical Engineering, VIA University, Horsens - Denmark, Bachelor’s degree.
- (2014-2018) Mechanical Engineering, Aarhus University - Denmark, Master's degree (attended).
- (2016-2018) IT Networks Engineering,  BAAA School of technology, Aarhus - Denmark, AP degree.

# Experience

## (2018-present) System administrator, Combell Group, Soﬁa, Bulgaria

On my current position, as part of Combell’s Network Operations Center in Soﬁa, I have gained experience in the following fields:

### Managing `.deb` boxes

- `pvresize /dev/sdb; lvextend -l+100%FREE /dev/mapper/vg02-lv_var; resize2fs /dev/mapper/vg02-lv_var`
- `nc -v -w 2 -z <IP> 22 80 443 3306`
- `for file in /proc/*/status ; do awk '/VmSwap|Name/{printf $2 " " $3}END{ print ""}' $file; done | sort -k 2 -n -r | less`
- `strace -p $(ps -ef |grep fpm | grep -v master | awk {'print $2'}| tr '\n' ' ' | xargs | sed 's/ / -p /g')`

### Managing `.exe` boxes

- Migrating customer websites to our shared hosting platform;
- Managing cloud infrastructure using VMware vCenter;
- Managing system level fs permissions and network interfaces;
- Writing shell and Python scripts for automating routine tasks;
- Web server adminstration (including proxy and cache servers);
- Database server administration (including replication setups);

## (2018–2018) Junior System administrator, Fleten.net A/S, Braedstrup, Denmark

Building a bare metal Ubuntu cloud running the OpenStack framework. The resulting private cloud implemented a software deﬁned storage solution, tenant network isolation and a high-density LXC virtual server environmentBuild and test an OpenStack deployment. Experience with MAAS and Juju.

- `sudo apt update; sudo apt upgrade -y; sudo apt install <package>`;
- `sudo useradd $USER; sudo groupadd $GROUP; sudo chown $USER:$GROUP <filename>`;
- Deploying and managing a new, internal IT ticket system;
- Deploying OpenStack private cloud into production;

## (2017–2018) Freelance web development, Self-employed, Aarhus, Denmark

As a freelancer I have been working with popular web technologies, such as RESTful APIs and MVC architectures. My primary choice of technologies was Python/Flask & Jinja2 tmplating. Tasks icluded:

- Working with databases (MySQL);
- Working with Python on the `import flask` framework;
- Working with `import requests` python module;
- Working with `import json` python module;
- Working with `import sys, subprocess` python modules;
