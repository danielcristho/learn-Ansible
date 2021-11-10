##Install and managing service
```
$ ansible all -b -m apt -a "name=nginx state=latest"
$ ansible all -b -m service -a "name=nginx state=started enabled=yes"
$ ansible all -b -a "systemctl status nginx"

```
##stop and remove service
```
$ ansible all -b -m service -a "name=nginx state=stopped"
$ ansible all -b -m apt -a "name=nginx state=absent purge=yes autoremove=yes"

```

