# hardening-server
This repository contians some of security tips to harden your LINUX server 
How to run it ? 
first create a master playbook to call this role like this 
$ cat MAyman.harden.yml
--- # Master Playbook For Hardening Servers
- hosts: web    #This group locate in host inventory '/etc/ansible/hosts'
  user: mayman  #make sure this user in a sudo file
  become: yes
  connection: ssh
  roles:
    - MAyman.harden
 
 then, use $ ansible-playbook --list-tags MAyman.harden.yml # to list all tags, the result like this "TASK TAGS: [login_defs, ntpd, password_policy, sha512, usb_storage]" 
 
 to run a specific tag use $ ansible-playbook MAyman.harden.yml --tags "password_policy,sha51"
 to run all tags use $ ansible-playbook MAyman.harden.yml
