# ansible-django-ormuco

## Steps to install ormuco aplication 

#### 1- install ansible 
      $ sudo apt-get install ansible 
      $ sudo apt-get update && sudo apt-get -y upgrade
           
#### 2- generate a Key Pair for authentication without password
      $ cd ~/.ssh/
      $ ssh-keygen -t rsa -b 2048 -v     
      
      Enter file in which to save the key:key
      Enter passphrase (empty for no passphrase):nothing, empty
      
      $ ssh-copy-id -i key.pub root@your-ip-address
      $ sudo nano authorized_keys
      
      output-examle:
      ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAAX ...
      ssh-rsa AQCqFd4B798zz9Lu+a3jGjhVXBRx ...
           
#### 3- clone repository 
      $ cd /home
      $ git clone https://github.com/hariza17/ansible-django-ormuco.git
      
#### 4- edit ansible files
      $ cd ansible
      $ nano hosts
      
      output-examle:
      [servers]
      *159.203.128.87 ansible_user=root ansible_ssh_private_key_file=~/.ssh/key
          you ip 

#### 5- run ansible playbook
      $ cd ansible
      $ ansible-playbook -i hosts provision.yml


#### 6- enter to browser 
      https://your-ip
     
    

