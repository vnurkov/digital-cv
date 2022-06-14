# Curriculum vitae

## Education

- (2009-2013) Mechanical Engineering, VIA University, Horsens - Denmark, Bachelor’s degree
- (2014-2018) Mechanical Engineering, Aarhus University, Aarhus - Denmark, Master's degree (attended)
- (2016-2018) IT Networks Engineering, BAAA School of technology, Aarhus - Denmark, AP degree

## Professional experience

### (2018-present) System administrator, Combell Group, Soﬁa, Bulgaria

On my current position as a systems admin, I have gained experience in managing cloud infrastructure using VMware vCenter and OpenStack virtualization platforms and further experience in handling task such as:

#### Managing `.deb` boxes

- `pvresize /dev/sdb; lvextend -l+100%FREE /dev/mapper/vg02-lv_var; resize2fs /dev/mapper/vg02-lv_var`
- `nc -v -w 2 -z <IP> 22 80 443 3306`
- `for file in /proc/*/status ; do awk '/VmSwap|Name/{printf $2 " " $3}END{ print ""}' $file; done | sort -k 2 -n -r | less`
- `ps -o pid,user,%mem,command ax | sort -b -k3 -r`
- `strace -p $(ps -ef |grep fpm | grep -v master | awk {'print $2'}| tr '\n' ' ' | xargs | sed 's/ / -p /g')`
- `for x in $(cat iplist); do echo "Deny from ${x}" >> htaccess; done`

#### Managing `.exe` boxes

- `net start WMSVC`
- `%systemroot%\system32\inetsrv\appcmd recycle apppool /apppool.name:<NAME>`
- `netsh http show ssl`
- `Get-ChildItem -Recurse | Select-String "dummy" -List | Select Path`

#### Migrating customer websites to the shared hosting platform

- `rsync -av /var/www/html/ <IP>:/home/$USER/app`

#### Writing shell and Python scripts for automating routine tasks

```bash
for i in $(cat traffic_out | awk {'print $1'} | sort | uniq |sort -rn | head -n7)
do
  ADDR=$i
  iptables -I INPUT -s $ADDR -j DROP
  echo "Block ALL INPUT from " $ADDR " net DROPPED."
done
```

#### Managing `nginx` & `apache` servers (+proxy, +loadbalancer setups)

- `cat /path/to/access.log | awk {'print $1'} | sort | uniq -c | sort -rn | head -n15`
- `/usr/sbin/tcpdump -n -i any -s 0 -A tcp dst port 80`

#### Managing `mysql` & `elasticsearch`

- `find /var/mysqldata/ -name "cache*" -exec du -shx "{}" \; |grep -v K | sort -n -r`
- `curl localhost:9200/_cluster/health`
- `curl -XGET localhost:9200/_cluster/allocation/explain?pretty`
- `curl -XGET localhost:9200/_cat/shards?h=index,shard,prirep,state,unassigned.reason| grep UNASSIGNED`
- `curl -XPOST localhost:9200/_cluster/reroute?retry_failed=true`
- `curl localhost:9200/_search?pretty`

### (2018–2018) Junior System administrator, Fleten.net A/S, Braedstrup, Denmark

Building a bare metal Ubuntu cloud running the OpenStack framework. The resulting private cloud implemented a software deﬁned storage solution, tenant network isolation and a high-density LXC virtual server environmentBuild and test an OpenStack deployment. Experience with MAAS and Juju.

- `sudo apt update; sudo apt upgrade -y; sudo apt install <package>`;
- `sudo useradd $USER; sudo groupadd $GROUP; sudo chown $USER:$GROUP <filename>`;
- `openstack server list --all-projects |grep $INSTANCE`
- `openstack server show $VPSID`
- `openstack console url show $VPSID --spice`

### (2017–2018) Freelance web development, Self-employed, Aarhus, Denmark

As a freelancer I have been working with popular web technologies, such as REST APIs and Source control (Git). My primary choice of technologies was Python/Flask & Jinja2 templating. Experience gained in:

- Source control: `git add . ; git commit -m "MESSAGE"; git push -u origin <branch>`
- Working with databases (MySQL);
- Working with Python on the `import flask` framework;
- Working with `import requests` python module;
- Working with `import json` python module;
- Working with `import sys, subprocess` python modules;
