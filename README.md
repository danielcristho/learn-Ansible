# Ansible Ad Hoc
### Install and managing service
```yml
$ ansible all -b -m apt -a "name=nginx state=latest"
$ ansible all -b -m service -a "name=nginx state=started enabled=yes"
$ ansible all -b -a "systemctl status nginx"
```

### remove

```yml
$ ansible all -b -m service -a "name=nginx state=stopped"
$ ansible all -b -m apt -a "name=nginx state=absent purge=yes autoremove=yes"

```
## ansible  monitoring
```yml
$ ansible all -a "free -m"

$ ansible all -b -m apt -a "name=sysstat state=latest"
$ ansible all -a "mpstat -P ALL"

```
## gathering fact
```yml

$ ansible all -m setup
$ ansible all -m setup -a "filter=ansible_distribution"
$ ansible all -m setup -a "filter=*distribution*"

```
### manages file


#### upload file

```yml
$ nano test.txt
$ ansible all -m copy -a "src=test.txt dest=/home/ansible"
$ ansible all -a "cat /home/ansible/test.txt"

```
#### download file
```yml
$ ansible debian -m fetch -a "src=/home/ansible/test.txt dest=/home/user1/ flat=yes"
$ ansible all -m fetch -a "src=/home/ansible/test.txt dest=/home/user1/ flat=yes"
```




