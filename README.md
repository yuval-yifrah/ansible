
created an ansible playbook that runs on 2 machines and downloads each machine its proper services by the tags.  
to run it create 3 machines.  
one will be the playbook manager and the 2 others needs to have tags:  
a. Name – mysql-test-aws-<your_name>-01  
b. Service – mariadb1011-server  
c. Version – 10.11.13    
d. Restart – Sunday at 6:00 am  
e.managed - true  
<img width="318" height="294" alt="image" src="https://github.com/user-attachments/assets/37ccf9dc-fe50-4bb9-99bc-22c25923b7f7" />


7. Second instance should have the following tags:  
a. Name – nginx-test-aws-06  
b. Service – nginx  
c. Version – 1.28.0  
d. Restart – Saturday at midnight  
e.managed - ture
<img width="360" height="320" alt="image" src="https://github.com/user-attachments/assets/110bb681-6ba7-43f2-b485-7da3559e936a" />


copy the key.pem to your manager machine and run it like this:  
 ansible-playbook -i aws_ec2.yml playbook.yml --private-key=~/yuvaly1key.pem   
 
