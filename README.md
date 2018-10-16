# AnsibleContainerManagement

Prerequisites:

Ansible >= 2.7
python 2
docker-py python module
_________________________________________________________________________________________________________________________
Install docker-py :
pip install docker-py

To invoke the containers on local system , you have to run docker.py which is a dynamic inventory for ansible to fetch docker containers dynamically.
 
 chmod +x docker.py
 
 ./docker.py
 _______________________________________________________________________________________________________________________
 You can use ansible commnads to see more sorted output
 
 ansible-inventory -i docker.py --list
 
 _______________________________________________________________________________________________________________________
 To ping a running container 
 
 ansible all -m ping -i docker.py -c docker
 
 _______________________________________________________________________________________________________________________
 If the container is not reachable then you have to install python inside a container 
 
 ansible all -m raw -a "yum install python2 -y" -i docker.py -c docker <br>
 or <br>
 ansible <container_name> -m raw -a "yum install python2 -y" -i docker.py -c docker
 
 
 
