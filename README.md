# Ansibletower 3.8 installation 

1. Register in the redhat site to get the trial version of Ansible tower.

     https://www.redhat.com

2. Create the EC2 machine with ami-096fda3c22c1c990a with m4.large ( minimum)

3. Update the all the packages

        yum update
 
4.  Install the python3

         dnf install python3
  
5. check the python installaton and pip3 installation 
 
         python3 --version
         pip3 --version
 
6. Install the Ansible. Ansible tower 3.8 needs the <=  Ansible 2.9 version
 
        pip3 install ansible
 
7. check the ansible installation
 
            ansible --version
   
8. Download the anisble tower trial version from the redhat site or download from my s3 bucket .Place it on  /opt folder. ( install wget incase it is not installed)
 
           yum install wget
           wget https://devops2020.s3.amazonaws.com/ansible-automation-platform-setup-bundle-1.2.0-1.tar.gz
 
 
9.Untar it
  
     tar -xvf ansible-automation-platform-setup-bundle-1.2.0-1.tar.gz
  
10. Rename it to ansible tower
  
     mv -f ansible-automation-platform-setup-bundle-1.2.0-1 ansibletower
  
11. Go to inventory file which is in anisble tower folder and update the passords .Sample inverntoy file after entering the passwords
  
  [tower]
localhost ansible_connection=local

[automationhub]

[database]

[all:vars]
admin_password='ansibletower'

pg_host=''
pg_port=''

pg_database='awx'
pg_username='awx'
pg_password='ansibletower'
pg_sslmode='prefer'  # set to 'verify-full' for client-side enforced SSL


automationhub_admin_password='ansibletower'

automationhub_pg_host=''
automationhub_pg_port=''

automationhub_pg_database='automationhub'
automationhub_pg_username='automationhub'
automationhub_pg_password=''
automationhub_pg_sslmode='prefer'

 
12. Ran the setup.sh which is inside of the ansibletower folder 
 
13. Make sure that port 443 is opened and open the ansible tower url from the browser.
 
      https://<<serverip>>
          ansible tower credentials
          admin
          ansibletower
     
14. Upload the Manifest zip license file after the login into the anisble tower     
 
 
  
 
    
