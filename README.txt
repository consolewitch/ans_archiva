This role implements the instructions layed out in the following article
http://archiva.apache.org/docs/2.2.0/adminguide/webapp.html

Preperation:
============

*The ansible EC2 module requires boto:  sudo apt-get install python-boto
*Several of the local_action plays reqiure that the box on which you're executing this playbook have maven installed
*You'll need to creat an IAM account with the name _ansible and give it permissions to EC2
*You will need a key-pair installed in your EC2 console. when you pass the key_name variable, it wants the name in your ec2 console.

Versions
========

tomcat version 7.0.64
java JDK version 1.7.0_76



Calling this playbook:
the provision role uses ansible-vault. To call it as part of the ansible-playbook command use the following format:
ansible-playbook site.yml --vault-password-file ~/.vault_pass.txt

To Do
=====
Replace hard-coded test values with variables / defaults
configure heap size as part of startup play
write tomcat start / tomcat stop tasks for archiva role
provision an s3 share for the actual artifact repository
