# 🌐 EC2 Website Hosting – Student Survey Web Page  
This project demonstrates how to host a static website using Amazon EC2 and Apache. It includes a student survey form, a landing page styled with W3.CSS, and a custom 404 error page. The site was originally hosted on AWS S3 and later migrated to EC2 for direct web server hosting.  

## 📌 Description  
A simple HTML-based student survey site deployed on an EC2 Ubuntu instance using Apache. This project showcases AWS S3 static website hosting and the end-to-end deployment process using an EC2 virtual machine.  

## 🛠️ Tech Stack  
- HTML5, CSS  
- Apache2 on Ubuntu  
- AWS EC2 (Ubuntu)  
- AWS S3 (initial static hosting)  

## 📁 Key Files  
- `studentClassIndex.html` – Home page with profile info and navigation  
- `StudentSurvey.html` – Styled feedback form for CS department  
- `error.html` – Custom 404 error page  
- `myphoto.jpg`, `map2.jpg` – Static image assets  

## 🚀 Deployment Guide  

### ✅ Hosting on S3  
1. Created an S3 bucket named `swe-645-assignment1` in the `us-east-2` region.  
2. Enabled static website hosting and uploaded HTML/image files.  
3. Site was accessible via public S3 URL.  

### ☁️ Hosting on EC2 (Ubuntu + Apache)  
1. Launched a new EC2 instance using Ubuntu.  
2. Opened required ports: SSH (22), HTTP (80), HTTPS (443).  
3. Connected to EC2 using SSH.  
4. Ran the following setup steps:  
```bash
mkdir deepika
cd deepika
wget https://github.com/deepikatendulkar1/Ec2-Website-Hosting/archive/refs/heads/main.zip
sudo apt install unzip
unzip main.zip
cd Ec2-Website-Hosting-main
sudo mkdir -p /var/www/html
sudo chown -R $USER:$USER /var/www/html
mv * /var/www/html
cd /var/www/html
sudo apt update
sudo apt install apache2
mv StudentSurvey.html index.html
sudo chown www-data:www-data index.html
sudo chmod 644 index.html
sudo systemctl start apache2


The site was previously accessible via the EC2 public IP address. Hosting has since expired due to AWS credits expiring.

📬 Contact
📧 deepikatenduulkar5@gmail.com
🔗 LinkedIn: https://www.linkedin.com/in/deepika-tendulkar-a88bb8166/
Developed as part of SWE 645 coursework at George Mason University. Demonstrates basic website hosting using AWS infrastructure.
