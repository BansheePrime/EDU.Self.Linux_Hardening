## ssh key error solution:
edit : ~/.ssh/config 
```
host 192.168.56.2*
     StrictHostKeyChecking no
     UserKnownHostsFile /dev/null
```

### ansible adhoc command:
```
ansible all -i inventory.yaml -a 'sudo --version'
```

