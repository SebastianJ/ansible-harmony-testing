## Usage

Clone the repo:
```
git clone https://github.com/SebastianJ/ansible-harmony-testing.git && cd ansible-harmony-testing.git
```

Install roles using ansible galaxy:
```
ansible-galaxy install --role-file requirements.yml --roles-path roles
```

Spin up a new VPS/server, replace IP_ADDRESS with the ip address of your new host.


### Using authorized keys
```
ANSIBLE_STRATEGY=free ansible-playbook --inventory IP_ADDRESS, playbook.yml --extra-vars "ansible_ssh_user=root"
```

### Using a password
```
ANSIBLE_STRATEGY=free ansible-playbook --inventory IP_ADDRESS, playbook.yml --extra-vars "ansible_ssh_user=root ansible_ssh_pass=pass"
```
