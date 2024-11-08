# Apache

## Introduction

This is an introduction for apache for DAW homework by me the one and only **Mohamed**.

Apache is a web server software that is responsible for accepting HTTP requests from visitors and sending them back the requested information in the form of web pages.
Or in simpler terms, it allows visitors to view content on the website.1 
Originally based on the NCSA HTTPd server, development of Apache began in early 1995 after work on the NCSA code stalled. Apache played a key role in the initial growth of the World Wide Web,[11] quickly overtaking NCSA HTTPd as the dominant HTTP server. In 2009, it became the first web server software to serve more than 100 million websites.2
### Some alternatives to Apaches include:

#### NGINX
- NGINX is a high-performance, open-source web server and reverse proxy. It is known for its ability to handle a large number of concurrent connections efficiently, making it a popular choice for high-traffic websites. NGINX can also function as a load balancer, HTTP cache, and reverse proxy server.

#### LiteSpeed
- LiteSpeed is a commercial web server with an open-source version called OpenLiteSpeed. It's optimized for speed and security, offering a high-performance alternative to Apache. It has built-in caching and supports features like HTTP/3 and QUIC for faster content delivery.

#### Caddy
- Caddy is a modern, open-source web server that comes with automatic HTTPS by default. It is simple to configure and designed to be easy to use, with a focus on modern web applications. Caddy is often used for developers looking for a hassle-free server with automatic SSL management.

#### Cherokee
- Cherokee is a high-performance, lightweight web server with a focus on ease of use. It supports a wide range of protocols, including HTTP/2, and is optimized for low resource usage, making it suitable for both small and large-scale deployments.

## Motivation

This project was made to learn how to install and work with apache.

## Configuration

### Creating My Own Website
- Creating a folder for our new website in /var/www/ by running  
![Screenshot from 2024-11-08 16-21-15](https://github.com/user-attachments/assets/1d1c7009-db1d-4fb4-a75d-2a6c40887ff9)
- Let’s go into our newly created directory  
![Screenshot from 2024-11-08 16-19-18](https://github.com/user-attachments/assets/cae572d8-ca3c-4efd-a4a7-c3165bf8d2fc)
- Lets create an HTML file  
![Screenshot from 2024-11-08 16-27-27](https://github.com/user-attachments/assets/f742d918-66a8-49ab-954b-005dea17f9dd)
- The code used in this HTML  
![Screenshot from 2024-11-08 16-28-45](https://github.com/user-attachments/assets/7ccc5ce2-e787-4e51-a908-b56d74b3214c)

### Setting up the VirtualHost Configuration File
- We start this step by going into the configuration files directory  
![Screenshot from 2024-11-08 16-38-34](https://github.com/user-attachments/assets/894b7846-59ba-4d99-834d-fd761bfe485b)
- Since Apache came with a default VirtualHost file, let’s use that as a base.  
![Screenshot from 2024-11-08 16-40-35](https://github.com/user-attachments/assets/b5c3827e-72f4-479d-8ee5-757d89140e7f)
- Now we edit the configuration file  
![Screenshot from 2024-11-08 16-49-44](https://github.com/user-attachments/assets/ec8ff112-a1a6-435b-9570-2a7221852259)
- We uncomment the ServerName and change it, and We also want the DocumentRoot directive to point to the directory our site files are hosted on.  
![Screenshot From 2024-11-08 18-07-32](https://github.com/user-attachments/assets/4b0c1ca2-5931-4b08-bc80-d08d66ab2e40)


### Activating VirtualHost file
- we need to activate the virtual hosts configuration file to enable it  
![Screenshot from 2024-11-08 16-55-15](https://github.com/user-attachments/assets/de227a84-1e9c-422d-825d-2a242a8513c8)
- To load the new site, we restart Apache by typing  
![Screenshot from 2024-11-08 16-56-41](https://github.com/user-attachments/assets/f10b5cc3-7431-4280-89ba-96837e6c4b63)
- End result  
![Screenshot from 2024-11-08 17-30-17](https://github.com/user-attachments/assets/d641d000-66bd-4dc3-9fa1-f374d9d5f6b1)
- If the url doesn't work then go to **/etc/hosts** in your files, and add **127.0.1.2 gci.example.com** after the 127.0.1.1 Ubuntu
![Screenshot From 2024-11-08 18-12-20](https://github.com/user-attachments/assets/beecb31c-5fe4-4185-be8a-54a581d5b4b4)

## Conclusion
In this project, I explored the installation and configuration of the Apache web server, gaining hands-on experience in setting up a basic website and customizing the server to serve my content. Apache's flexibility and widespread use make it an essential tool for web developers, and through this process, I learned how to create a custom site folder, configure the VirtualHost settings, and troubleshoot common issues related to Apache configuration.

## Annexes

### Annex A: Detailed Installation Steps
1. **Step 1**: Install Apache on Ubuntu:
   ```
   sudo apt update
   sudo apt install apache2
   ```
2. **Step 2**: Check if Apache is running:
   ```
   systemctl status apache2
   ```
### Annex B: Example Configuration Files
   The default VirtualHost configuration file typically looks like this:
   ```
    <VirtualHost *:80>
        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/html
        ServerName example.com
    </VirtualHost>
  ```

### Explanation of the Annexes:

- **Annex A** contains step-by-step instructions for installing Apache, which is essential if you're following along with the project.
- **Annex B** provides an example of an Apache `VirtualHost` configuration file, which is central to setting up Apache to serve your website.

# Bibliography
- What is Apache (https://www.greengeeks.com/blog/what-is-apache/#What_Is_Apache)
- Apache server (https://en.wikipedia.org/wiki/Apache_HTTP_Server)
- resolving the problem (https://discourse.ubuntu.com/t/install-and-configure-apache/13955)
- Followed steps (https://ubuntu.com/tutorials/install-and-configure-apache#1-overview)
