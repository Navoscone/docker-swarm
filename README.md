# Docker CE Swarm 18.09

## Clone do Projeto

<pre>
$ https://github.com/Navoscone/docker-swarm
</pre>

## Arquivo hosts (Ajuste os IP's / Keypair)
<pre>
[docker-ce]
master1     ansible_ssh_host=ENDEREÇO IP
master2     ansible_ssh_host=ENDEREÇO IP
master3     ansible_ssh_host=ENDEREÇO IP

worker1     ansible_ssh_host=ENDEREÇO IP
worker2     ansible_ssh_host=ENDEREÇO IP
worker3     ansible_ssh_host=ENDEREÇO IP

[swarm-master]
master1

[swarm-manager]
master2
master3

[swarm-worker]
worker1
worker2
worker3

[all:vars]
ansible_ssh_user=ubuntu
ansible_ssh_private_key_file=CAMINHO ATÉ A CHAVE
</pre>
## Running Playbook!
<pre>
ansible-playbook play-docker-swarm.yml -i hosts
</pre>
