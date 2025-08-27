# ansible

created an ansible playbook that runs on 2 machines and downloads each machine its proper services by the tags.  
to run it create 3 machines.  
one will be the playbook manager and the 2 others needs to have tags:  
a. Name – mysql-test-aws-<your_name>-01  
b. Service – mariadb1011-server  
c. Version – 10.11.13    
d. Restart – Sunday at 6:00 am  
e.managed - true  

7. Second instance should have the following tags:  
a. Name – nginx-test-aws-06  
b. Service – nginx  
c. Version – 1.28.0  
d. Restart – Saturday at midnight  
e.managed - ture

copy the key.pem to your manager machine and run it like this:  
 ansible-playbook -i aws_ec2.yml playbook.yml --private-key=~/yuvaly1key.pem   
 
