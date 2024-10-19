# Health Website Deployment using Vagrant

This repository contains the code and resources for a health-themed website deployed using Vagrant.

## Deployment Steps

This section outlines the steps taken to deploy the website.

### Prerequisites

- Vagrant
- VirtualBox
- Git

### Commands Used

1. **Set the hostname**:
   ```bash
   vim /etc/hostname
   hostname HealthCenter
   exit
2. **Install necessary packages**:
yum install httpd wget vim unzip zip -y

3. **Start and Enable Apache Server**
 
systemctl start httpd
systemctl enable httpd

4. **Download the Website Template**

Note: I have taken free website template from https://www.tooplate.com/

cd /tmp/
wget https://www.tooplate.com/zip-templates/2098_health.zip

5. **Unzip the Downloaded Template**

unzip 2098_health.zip
cd 2098_health/

6. **Copy Files to the Web Directory**

cp -r * /var/www/html/

7. **Restart Apache Server

systemctl restart httpd

Accessing the Website

To View the website, open a web browser and navigate to:

http://http://192.168.33.10/
