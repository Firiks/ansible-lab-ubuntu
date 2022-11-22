# Testing lab for ansible

## Setup
- `run docker-compose up`
- must add fingenprint first to be able to use ansible (just ssh into each target machine):

- `ssh root@server01`
- `ssh root@server01`
- `ssh root@server01`

## ansible config
`/etc/ansible/ansible.cfg`

## default hosts
`/etc/ansible/hosts`

## ansible basic commands
`ansible <hosts> - a <command>`

`ansible all -a "/sbin/reboot"`

`ansible <hosts> - m <module>`

`ansible target1 -m ping`

## run ansible-playbook
`ansible-playbook <playbook-name.yml>`

## run playbook using custom inventory file
`ansible-playbook -i hosts playbook.yml`

## ping using hosts file
`ansible target -m ping -i hosts`

## list modules
`ansible-doc -l`