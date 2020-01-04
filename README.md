# Ansible-Roles-LAMP-Deploy
Install ansible with help of below link for ubuntu machine:
https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-18-04

Change Hostname with help of below link:
https://linuxize.com/post/how-to-change-hostname-on-ubuntu-18-04/
sudo hostnamectl set-hostname ansible-manager

Folder structure of Ansible with Roles

├── README.md
├── inventory
├── playbook.yml
└── roles
    ├── apache2
    │   ├── files
    │   └── tasks
    │       └── main.yml
    └── mysqldb
        ├── files
        │   └── users.sql
        └── tasks
            └── main.yml

Verify or Ping with below command:
ansible -i inventory -m ping all
 or 
ansible -i inventory -m ping apache2
ansible -i inventory -m ping dbserver

Run Playbook:
ansible-playbook -i inventory playbook.yml
