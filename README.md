# Ansible Ad Hoc
### Install and managing service
```
$ ansible all -b -m apt -a "name=nginx state=latest"
$ ansible all -b -m service -a "name=nginx state=started enabled=yes"
$ ansible all -b -a "systemctl status nginx"

### remove
```
$ ansible all -b -m service -a "name=nginx state=stopped"
$ ansible all -b -m apt -a "name=nginx state=absent purge=yes autoremove=yes"

```
## ansible  monitroing
```
$ ansible all -a "free -m"

$ ansible all -b -m apt -a "name=sysstat state=latest"
$ ansible all -a "mpstat -P ALL"

```

