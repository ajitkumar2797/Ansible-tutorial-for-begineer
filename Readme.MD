# Install Ansbile using script.sh

Swtich to Root User 
sudo su

```bash
cd Install-Ansbile/
chmod +x script.sh
sh script.sh
```

# Install Ansible using cmd 

```bash
sudo su
yum update -y 
yum install ansible -y 
ansible --version
```
![image](https://user-images.githubusercontent.com/63657725/176108690-f376e72d-7d03-4b69-b3d5-cffbbab07b9b.png)


# Demo: Install Apache web server on Target 1 and Target 2 machines

1. Copy the index.htmls files in the following path.
```bash
cd Demo-Ansible/webpage-files/
cp -r Demo-Ansible/webpage-files /home/ec2-user/
```
2. Try a ping test from Master node to Target machines

``` bash
cd Demo-Ansible/
cat inventory.txt

# To perfomr a ping test to the Target machines:
ansible all -m ping -i inventory.txt
```
![image](https://user-images.githubusercontent.com/63657725/176107281-ded3f441-a271-477e-aa40-d11128290d38.png)

 
 3. Install Apache web server on the Target Machines
 
 ```bash
 cd Demo-Ansible/
 
 ansible-playbook install-apache-server.yaml -i inventory.txt
 ```
 ![image](https://user-images.githubusercontent.com/63657725/176107805-f97f7dd6-0e3a-484e-a65f-c3c0d2994c9b.png)
 
 The web Page will look like this:
 ![image](https://user-images.githubusercontent.com/63657725/176107939-d97ff958-ca0c-447b-b518-d069d680bf8e.png)
 
 
 
# Demo: Uninstall Apache web server on Target 1 and Target 2 machines

``` bash
 cd Demo-Ansible/
 ansible-playbook uninstall-apache-server.yaml -i inventory.txt
 ```
  ![image](https://user-images.githubusercontent.com/63657725/176108289-54acc6f4-b791-44b5-9def-add0d24ebced.png)




