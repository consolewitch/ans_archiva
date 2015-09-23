Preperation:
============

*The ansible EC2 module requires boto:  sudo apt-get install python-boto
*You'll need to creat an IAM account with the name _ansible and give it permissions to EC2
*You will need a key-pair installed in your EC2 console. when you pass the key_name variable, it wants the name in your ec2 console.




Calling this playbook:
the provision role uses ansible-vault. To call it as part of the ansible-playbook command use the following format:
ansible-playbook site.yml --vault-password-file ~/.vault_pass.txt
