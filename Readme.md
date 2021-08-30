To run this, assuming you have `ansible` installed - first change the IP address to match the primary interface on your server in `install_docker.yml` on the line (I'm sure there's a more 'ansible' way to get the IP...) :
```
shell: docker swarm init --advertise-addr=192.168.1.34
```

Then run the playbook against the same IP :
```bash
ansible-playbook install_docker.yml -i 192.168.1.34,
```

(Note the trailing `,`)
