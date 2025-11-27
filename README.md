🛠️ Step-by-Step EC2 + Nginx Implementation<br>
<br>Step 1: Launch EC2<br>

<br>-AMI: Amazon Linux 2<br>

-Instance Type: t2.micro (Free Tier eligible)<br>

<br>Security Group Rules:<br>

-SSH (22): Your IP only → for secure access<br>

-HTTP (80): Anywhere → so you can access your website<br>

-Tip: Leave HTTPS (443) disabled for now — optional for testing.<br>

<br>Step 2: SSH into EC2
<br> ssh -i key.pem ec2-user@ public-ip-address <br>

<br>Install Apache<br>
- sudo yum update -y <br>
- sudo yum install httpd -y <br>
- sudo systemctl start httpd <br>
- sudo systemctl enable httpd <br>

<br>Deploy your website<br>
- sudo su<br>
- cd /var/www/html<br>
- echo "Welcome to My EC2 Website!" > index.html<br>

<br>
http://<EC2-public-ip>
