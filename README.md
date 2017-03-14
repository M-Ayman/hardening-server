hardening-server
===============



This role Install and configure some of security tips to harden your LINUX server 

Requirements
------------

This role requires Ansible 2.2 or higher


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

	- hosts: all
      remote_user: root
      roles:
      - MAyman.harden

    

	then, use $ ansible-playbook --list-tags MAyman.harden.yml 
	# to list all tags, the result like this "TASK TAGS: [login_defs, ntpd, password_policy, sha512, usb_storage]" 
 
 to run a specific tag use $ ansible-playbook MAyman.harden.yml --tags "password_policy,sha51"
 to run all tags use $ ansible-playbook MAyman.harden.yml

Author Information
------------------

www.linkedin.com/in/m0hamed-ayman


