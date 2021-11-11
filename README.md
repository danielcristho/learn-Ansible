# Ansible Ad Hoc
### Install and managing service
```
$ ansible all -b -m apt -a "name=nginx state=latest"
$ ansible all -b -m service -a "name=nginx state=started enabled=yes"
$ ansible all -b -a "systemctl status nginx"
```

### remove

```
$ ansible all -b -m service -a "name=nginx state=stopped"
$ ansible all -b -m apt -a "name=nginx state=absent purge=yes autoremove=yes"

```
<<<<<<< HEAD
### ansible  monitroing
=======
## ansible  monitoring
>>>>>>> 0453b378f784019dd5caaab1f53645cb007b2773

```
$ ansible all -a "free -m"

$ ansible all -b -m apt -a "name=sysstat state=latest"
$ ansible all -a "mpstat -P ALL"

```
### gathering fact
```

$ ansible all -m setup
$ ansible all -m setup -a "filter=ansible_distribution"
$ ansible all -m setup -a "filter=*distribution*"

```
### manages file

#### upload file

```
$ nano test.txt
$ ansible all -m copy -a "src=test.txt dest=/home/ansible"
$ ansible all -a "cat /home/aguna/test.txt"

```

#### download file
```
$ ansible debian -m fetch -a "src=/home/ansible/test.txt dest=/home/user1/ flat=yes"

```




