## Create L.E.M.P STACK USING AWS
### The LEMP Stack is another popular stack (Stack of technologies working together) to deploy a websolution but instead of APACHE as the web server we will use NGINX

1. First we deploy an Linux Instance on AWS (In this Case using an Ubuntu AMI)
2. Next we update our Linux machine using the `sudo apt update` command
![update cmd](sudoaptupdate.jpg)
3. We then install NGINX using `sudo apt install nginx` command 	![nginxinstall](sudoaptinstallnginx.jpg)
4. Confirm it's installed using `sudo systemctl status nginx` If it shows active running in Green you have now launched a web server in the cloud! ![NGINX Status](nginxrunning.jpg)
5. Type in http://<Public IP address of Instance running web server>:80 and you should see: ![NGINX Running from IP Address](nginxrunning2.jpg)
6. Now we will install our Database we will be using MySQL use the `sudo apt install mysql-server` ![DB Install](mysqlinstall.jpg)
7. Once install use cmd `sudo mysql` to login into the Database. You will be the Admin user ROOT
8. Once inside the DB  You will want to run an Pre-installed Security script that will Lockdown some not secure default settings and access to the DB use `ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Create your PassWord here'; 