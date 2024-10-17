# Cloud-Automation
Provisioning of Two Digital Ocean Droplets as WordPress Website Platforms Using Ansible Automation Tool

This project aims to automate the deployment of a WordPress site to the cloud provider Digital Ocean. We will utilize Ansible, a software tool that facilitates RESTful API calls, to streamline this process. The deployment will be executed on a virtual machine running CentOS 7. A script will be developed to direct Ansible in creating Droplets (virtual machines) that will operate as WordPress sites.

**Resources used**:
- VMWare Fusion (for Mac)
- CentOS 7 (minimal)
- Digital Ocean
- Ansible

  # Setting Up CentOS7/Ansible:
This is the process of setting up your CentOS VM to enable it as your Ansible server.
  
- Once your in your Centos VM run a yum update
  
 ![image](https://github.com/user-attachments/assets/cbe5b4b0-b8d5-4c0d-b641-1481febfa250)

-	Install epel-release

![image](https://github.com/user-attachments/assets/606172d3-cac9-4758-9f4a-6833fb71f75d)

  
-	Install Ansible 

![image](https://github.com/user-attachments/assets/cf26a377-fc82-4448-9339-bf460000bc11)

  
-	Install python-pip

![image](https://github.com/user-attachments/assets/3bc021a5-b577-46fd-956e-88d800f6faec)

-	Navigate to ansible config file in the /etc/ansible/ directory

![image](https://github.com/user-attachments/assets/54a16cfd-3efd-41de-9d15-a3fb10245428)

 
-	At the bottom of the file add “[localhost] localhost ansible_connection=local” then save the file

![image](https://github.com/user-attachments/assets/c156714b-557c-4312-9ea1-892cae8022d5)
  
-	Generate a RSA key to add to your Ansible script by running the command “ssh-keygen -t rsa” and remember the path

![image](https://github.com/user-attachments/assets/55ef2eba-d0f0-4c33-aa9d-958e7c184447)


# Obtaining Digital Ocean token
Now we will also create a Digital Ocean token, take we may enable it to connect with our machine to instruct it on what to do.
-	Go to Digital Ocean click API then click “Generate Token”

![image](https://github.com/user-attachments/assets/03407dc7-1e41-424b-9685-6005f71d6b03)

-	Assign it a name of your choice and choose an expiration time

![image](https://github.com/user-attachments/assets/b3608275-382c-4422-8a21-8d37775b9f70)
 
-	Choose generate token and ensure you save/copy the token, as it will get added to the script

# Running Script & Configuring WordPress
Upon the final step, this is where you will ultimately run the Ansible playbook and access the Droplet to configure WordPress. _(sample of my script located here)_
 -	Once you created your script run it by running “ansible-playbook [name of script]" Once it completes you'll get a recap of the playbook indicating either success, failure, or changes.

![image](https://github.com/user-attachments/assets/6da6092e-ecf7-45dc-8f87-8c7e32dfd461)
	 
-	Go to you to access the WordPress site to configure ex: http://192.13.134.140/wordpress

![image](https://github.com/user-attachments/assets/6fc65046-741d-4ccd-a2c8-36cd9b57c494)
  
-	Once you picked a language, you’ll enter a setup screen

![Picture1](https://github.com/user-attachments/assets/00a2ac17-7b87-487f-970c-07123c6cd170)

-	Fill out the required information and clicked install WordPress
-	Once installed log in

![Picture2](https://github.com/user-attachments/assets/6d4cfb28-3958-40f8-aeef-0ef3970d228d)
 
-	Congratulations you installed and configured WordPress
-	You should see the home screen like this

![Picture3](https://github.com/user-attachments/assets/f1f2bde1-c034-4534-9ea8-920f81f5aabf)
	  
