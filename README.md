## basic operations
```
ansible all -m ping
ansible all -a "date"
ansible all -a "whoami"

```

## root operations
```
ansible all -b -a "whoami"
ansible all -b -a "fdisk -l"

```
