# Commands Used

## SSH into EC2
ssh -i key.pem ubuntu@<public-ip>

## Install Nginx
sudo apt update
sudo apt install nginx -y

## Start Nginx
sudo systemctl start nginx
sudo systemctl enable nginx

## Check Status
sudo systemctl status nginx

## Git Commands
git init
git add .
git commit -m "Initial commit"
git push


