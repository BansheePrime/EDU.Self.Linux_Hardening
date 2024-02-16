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

### running app playbook
ansible-playbook ../01_playbooks/app_playbook.yaml -i inventory.yaml

### vagrant ssh trail and tribs
```bash
sudo sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config;

sudo systemctl restart sshd;
```

### my solution
ssh-copy-id to localhost

### PerformanceTest Linux
<https://www.passmark.com/support/pt_linux_faq.php>
<https://www.passmark.com/downloads/bitlinux.tar.gz>
