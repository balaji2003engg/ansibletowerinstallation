# ansibletower 3.8 installation 

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
 
 6. Install the Ansible 
 
        pip3 install ansible
 
 7. check the ansible installation
 
 ansible --version
   
 8. Download the anisble tower trial version from the redhat site or download from my s3 bucket on /opt folder. ( install wget incase it is not installed)
 
  yum install wget
  wget https://devops2020.s3.amazonaws.com/ansible-automation-platform-setup-bundle-1.2.0-1.tar.gz
 
 
 9.Untar it
  
  tar -xvf ansible-automation-platform-setup-bundle-1.2.0-1.tar.gz
  
  10. Rename it to ansible tower
  
  mv -f ansible-automation-platform-setup-bundle-1.2.0-1 ansibletower
 
    
