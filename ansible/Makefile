
.PHONY: run chroot ssh

all: run

run:
	env ANSIBLE_FORCE_COLOR=true ansible-playbook ${ARGS} -i hosts main.yml 2>&1 | /home/user/lolcat/lolcat

chroot:
	env ANSIBLE_FORCE_COLOR=true ansible-playbook -l nosuchlink-setup-chroot ${ARGS} -i hosts main.yml 2>&1 | /home/user/lolcat/lolcat

ssh:
	sshpass -p$(shell grep ansible_ssh_pass hosts|cut -d= -f2|tail -n1) ssh -o Port=2222 -o User=root 10.137.2.16
