# Install Ansbile using script.sh

Swtich to Root User 
sudo su

```bash
cd Install Ansbile/
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

# ansible all -m ping -i inventory.txt
![image](https://user-images.githubusercontent.com/63657725/176107281-ded3f441-a271-477e-aa40-d11128290d38.png)

```

 
