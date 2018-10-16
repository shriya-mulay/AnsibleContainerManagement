# AnsibleContainerManagement
To invoke the containers on local system , you have to run docker.py which is a dynamic inventory for ansible to fetch docker containers dynamically.
 
 chmod +x docker.py
 
 ./docker.py
_________________________________________________________________________________________________________________________
 You can use ansible commnads to see more sorted output
 
 ansible-inventory -i docker.py --list (It will fetch all the containers on your host)
 _______________________________________________________________________________________________________________________
TO ping a running container:

ansible all -m ping -i docker.py -c docker
_________________________________________________________________________________________________________________________
If it's not reachable you have to check for python module inside a container :
To install a python module 

ansible all -m raw -a "yum install python2 -y" -i docker.py -c docker<br>
or<br>
ansible <container_name> -m raw -a "yum install python2 -y" -i docker.py -c docker


 
