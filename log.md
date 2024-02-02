## copy one file to several directories with bash
```bash
for i in ./alma9/ ./alpine319/ ./debian12/ ./rocky9/ ./ubuntu2204/; do cp ./Vagrantfile ./ubuntu2204/; done
```

## removing alpine 3.18 and 3.19 from roster
## distro not cooperating with ssh and ansible (no python on board)
## this time I will not create my own box with alpint + python
rm -r ./alpine*

# distro: ip: ssh out port
AlmaLinux 9.3: "192.168.56.10": 2110
Debian 12: "192.168.56.12": 2112
Rocky 9: "192.168.56.13": 2113
Ubuntu 22.04 (LTS): "192.168.56.14": 2114

### ping
ansible all -i inventory.yaml -m ansible.builtin.ping

### phoenixnap about ssh troubles:
<https://phoenixnap.com/kb/ssh-permission-denied-publickey>  

###