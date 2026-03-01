# Task 1: EC2 Nginx Deployment

## Simple Definition

Deploying a static website on an EC2 instance using the Nginx web server. Nginx acts as the gateway to serve web content to users over the internet.


## Objective

To learn EC2 instance setup, SSH connectivity, and basic web server deployment using Nginx service.



## Ubuntu / Amazon Linux

### Steps

1. Launch an EC2 instance (Ubuntu or Amazon Linux).
2. Connect to the instance using SSH.
3. Update package index and install Nginx.
4. Start and enable the Nginx service.
5. Clone the website repository from GitHub (PMfolio is actually my portfolio website).
6. Clear default web root files and move repository content to /usr/share/nginx/html.
7. Configure Security Groups to allow inbound traffic on Port 80 (HTTP).

### Verification

* `systemctl status nginx`
* Accessing the EC2 Public IPv4 address in a web browser.


## Conclusion

The web server was successfully configured, and the static website is live on the EC2 instance.