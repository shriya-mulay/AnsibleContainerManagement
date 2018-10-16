# AnsibleContainerManagement

Prerequisites:

Ansible >= 2.7
python 2
docker-py python module

Install docker-py :
pip install docker-py

To invoke the containers on local system , you have to run docker.py which is a dynamic inventory for ansible to fetch docker containers dynamically.
 
 chmod +x docker.py
 
 ./docker.py
 
 You can use ansible commnads to see more sorted output
 
 ansible-inventory -i docker.py --list
 
