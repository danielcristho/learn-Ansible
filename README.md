## basic operations
```
$ ansible all -m ping
$ ansible all -a "date"
$ ansible all -a "whoami"

```

## root operations
```
$ ansible all -b -a "whoami"
$ ansible all -b -a "fdisk -l"
$ ansible all -b -a "reboot"

```

## shell module
```
$ ansible all -m shell -a "echo 'hello world' > /home/ansible/hello.txt"
$ ansible all -a "cat /home/ansible/hello.txt"
```

## raw module 
```
$ ansible all -m raw -a " ls /home/ansible"
```

