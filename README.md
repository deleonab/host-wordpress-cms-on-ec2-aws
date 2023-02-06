###### HOSTING A WORDPRESS WEBSITE WITH AWS EC2 

Our goal is to host a website for xxxxxx solicitors on an Amazon EC2 Instance

For this, we shall need the following resources
An EC2 Instance running on Linux. I will go for the t2.micro 
An elastic IP so that the IP address will persist if the instance is stopped or interrupted
SSH into the Instance and install the following:
Security group to allow SSH into our instance for software installation and bootstrapping if required
Security group to allow HTTP and HTTPS traffic from the internet
An SSL Certificate to encrypt inflight data
A Domain name and A record for forwarding to our Elastic IP

- Apache Webserver
- PHP 
- Mysql

Install Wordpress

Additional Tools
- Github for version control and to document our actions
- VSCode - Code/Text Editor

LAUNCH EC2
------
We shall go to the AWS console and launch an Instance

We shall name our instance InstanceNameOfChoice
Select Ubuntu for our AMI (My Preference today)
Instance type will be t2.micro
Security groups ingress 
SSH(Port 22) - Allow from your IP Adress only  xx.xx.xx.xx/32
http(Port 80) Allow All 0.0.0.0/0 
https(Port 443) Allow All 0.0.0.0/0

ATTACH ELASTIC IP
Instance public IP addresses change when the instance is stopped and relaunched. To avoid losing
the ip address to our application, we shall use an Elastic IP address and attach it to our EC2 Instance.

