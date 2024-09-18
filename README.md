<div align="center">

  <h3 align="center">Laravel Setup over AWS</h3>
  <p align="center">
    Assignment Result URL = https://bhrtest.coid.io/
    <br />
    <br />
  </p>

</div>

# Table of Contents

1. [EC2 Setup](#ec2-setup)
2. [RDS Setup](#rds-setup)
3. [Laravel Deployment](#laravel-deployment)
    - 3.1 [Nginx Setup](#nginx-setup)
    - 3.2 [PHP and PHP-FPM Setup](#php-and-php-fpm-setup)
    - 3.3 [Install Composer and Laravel Setup](#install-composer-and-laravel-setup)
4. [Domain Setup and SSL Deployment](#domain-setup-and-ssl-deployment)


## EC2 Setup

- create ec2 from aws console
![image](./doc/EC2.png )
- attach elastic ip to ec2
![image](./doc/EIP.jpeg )
## RDS Setup

- create Aurora Mysql RDS from aws console
![image](./doc/RDS1.png )
![image](./doc/RDS2.jpg )
![image](./doc/RDS3.jpg )
- Allow EC2 security group to RDS Access
![image](./doc/RDS-SG.png )
- Test DB Connection and create database
![image](./doc/RDS4.png )
## Laravel Deployment

### Nginx Setup
- connect EC2 with ssh and install nginx
![image](./doc/install-nginx.png )
- check nginx default page
![image](./doc/nginx-default-page.jpg )

### PHP and PHP-FPM Setup
- install php , php-fpm and php extensions
![image](./doc/install-php.png )

### Install Composer and Laravel Setup

- install composer and create laravel project with composer
![image](./doc/install-composer.png )
- Update database credentials in .env file
- Database migration
![image](./doc/laravel-setup-1.png )
- Nginx Config for Laravel
![image](./doc/laravel-setup-2.png )
- Web Serice User Permission for laravel storage
![image](./doc/laravel-setup-3.png )

## Domain Setup and SSL Deployment

- add dns record
![image](./doc/domain-1.png )
- install certbot for free ssl
![image](./doc/domain-2.png)
- add domain name in nginx config 
![image](./doc/domain-3.png )
- generate ssl with certbot cli
![image](./doc/domain-4.png )
- Final Result
![image](./doc/final.jpg )
