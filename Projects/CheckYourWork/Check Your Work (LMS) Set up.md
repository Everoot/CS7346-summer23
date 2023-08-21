# Check Your Work (LMS) Set up

## Step 1: Install Ubuntu

https://docs.moodle.org/402/en/Installing_Moodle

### Hardware

- Disk space: 200MB for the Moodle code, plus as much as you need to store content. 5GB is probably a realistic minimum.
- Processor: 1 GHz (min), 2 GHz dual core or more recommended.
- Memory: 512MB (min), 1GB or more is recommended. 8GB plus is likely on a large production server
- Consider separate servers for the web "front ends" and the database. It is much easier to "tune"

All the above requirements will vary depending on specific hardware and software combinations as well as the type of use and load; busy sites may well require additional resources. Further guidance can be found under [performance recommendations](https://docs.moodle.org/402/en/performance_recommendations). Moodle scales easily by increasing hardware.

For very large sites, you are much better starting with a small pilot and gaining some experience and insight. A "what hardware do I need for 50,000 user?" style post in the forums is highly unlikely to get a useful answer.



https://moodle.org/mod/forum/discuss.php?d=351259#:~:text=Re%3A%20Server%20Hardware%20Requirement%20for%20300%20User,-by%20Usman%20Asar&text=4%2Dcore%20CPU%20with%204GB,300%2B%20without%20changing%20the%20hardware.

If possible, 8GB RAM & database on separate SSD drive will ensure addition of another 300+ without changing the hardware.





Instance type: t2.large 2vCPU 8GiB Memory

Operating System: Ubuntu 20.04 LTS



![Screenshot 2023-07-14 at 22.57.40](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-14 at 22.57.40.png)

![Screenshot 2023-07-14 at 22.57.55](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-14 at 22.57.55.png)

![Screenshot 2023-07-14 at 23.04.02](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-14 at 23.04.02.png)

![Screenshot 2023-07-15 at 09.57.55](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 09.57.55.png)

## Step 2: Install Apache/MySQL/PHP

`sudo apt update`

`sudo apt-get install vim`

`sudo apt install apache2 mysql-client mysql-server php7.4 libapache2-mod-php` 

----

If this command not success, download them one by one.

`sudo apt-get install apache2`

`sudo apt-get install mysql-client`

`sudo apt-get install mysql-server`

` sudo apt-get install php7.4 `

`sudo apt-get install libapache2-mod-php`

------

![Screenshot 2023-07-15 at 09.59.28](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 09.59.28.png)

![Screenshot 2023-07-15 at 10.00.00](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.00.00.png)

![Screenshot 2023-07-15 at 10.00.51](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.00.51.png)



## Step 3: Install Additional Software

```
sudo apt install graphviz aspell ghostscript clamav php7.4-pspell php7.4-curl php7.4-gd php7.4-intl php7.4-mysql php7.4-xml php7.4-xmlrpc php7.4-ldap php7.4-zip php7.4-soap php7.4-mbstring
```



------

If this command not success, download them one by one.

`sudo apt install graphviz`

`sudo apt install aspell`

`sudo apt install ghostscript `

`sudo apt install clamav`

`sudo apt install php7.4-pspell php7.4-curl php7.4-gd php7.4-intl php7.4-mysql php7.4-xml php7.4-xmlrpc php7.4-ldap php7.4-zip php7.4-soap php7.4-mbstring `

----

![Screenshot 2023-07-15 at 10.04.38](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.04.38.png)



`sudo service apache2 restart `

`sudo apt install git`

![Screenshot 2023-07-15 at 10.05.10](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.05.10.png)



## Step 4: Download Moodle

`cd /opt`

`sudo git clone git://git.moodle.org/moodle.git`

`cd moodle`

`sudo git branch -a`

`sudo git branch --track MOODLE_400_STABLE origin/MOODLE_400_STABLE`

`sudo git checkout MOODLE_400_STABLE`

![Screenshot 2023-07-15 at 10.08.14](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.08.14.png)



## Step 5: Copy local repository to /var/www/html/

`sudo cp -R /opt/moodle /var/www/html/`

`sudo mkdir /var/moodledata`

`sudo chown -R www-data /var/moodledata`

`sudo chmod -R 777 /var/moodledata`

`sudo chmod -R 0755 /var/www/html/moodle`

![Screenshot 2023-07-15 at 10.09.08](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.09.08.png)

## Step 6: Setup MySQL Server

`sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf`

![Screenshot 2023-07-14 at 23.46.42](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-14 at 23.46.42.png)

![Screenshot 2023-07-15 at 10.10.52](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.10.52.png)

-----

For MySQL Ver < 8.0, the three settings below are needed.

```
default_storage_engine = innodb
innodb_file_per_table = 1
innodb_file_format = Barracuda
```

---

`sudo service mysql restart`

``sudo mysql -u root -p`` 

ubuntu default password is none, just return is ok.

` CREATE DATABASE moodle DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;`

`create user 'moodledude'@'localhost' IDENTIFIED BY 'passwordformoodledude';`

`GRANT SELECT,INSERT,UPDATE,DELETE,CREATE,CREATE TEMPORARY TABLES,DROP,INDEX,ALTER ON moodle.* TO 'moodledude'@'localhost';`

`quit;`

![Screenshot 2023-07-15 at 10.12.35](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.12.35.png)

![Screenshot 2023-07-15 at 12.12.44](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 12.12.44.png)



## Step 7: Complete Setup

`sudo chmod -R 777 /var/www/html/moodle`

![Screenshot 2023-07-15 at 10.14.38](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.14.38.png)

![Screenshot 2023-07-15 at 10.14.05](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.14.05.png)

`sudo vi /etc/apache2/sites-available/000-default.conf`

`sudo service apache2 restart`

![Screenshot 2023-07-14 at 23.54.13](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-14 at 23.54.13.png)

![Screenshot 2023-07-15 at 00.11.43](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 00.11.43.png)

![Screenshot 2023-07-15 at 10.28.24](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.28.24.png)

------

Open your browser and go to http://IP.ADDRESS.OF.SERVER

![Screenshot 2023-07-15 at 10.28.46](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.28.46.png)

![Screenshot 2023-07-15 at 10.16.50](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.16.50.png)

Follow the prompts:

####Change the path for moodledata

`/var/moodledata`

![Screenshot 2023-07-15 at 10.30.27](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.30.27.png)



#### Database Type

Choose: mysqli

![Screenshot 2023-07-15 at 10.30.51](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.30.51.png)



#### Database Settings

Host server: localhost

Database: moodle

User: moodledude (the user you created when setting up the database)

Password: passwordformoodledude (the password for the user you created)

Tables Prefix: mdl_

![Screenshot 2023-07-15 at 10.31.53](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.31.53.png)





![Screenshot 2023-07-15 at 10.32.10](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.32.10.png)



需要修改权限

-----

how to change ubuntu password

`sudo su -`

`passwd`

`exit`

cs123456

-----

`cd /var/www/html/moodle `

`sudo cp config-dist.php config.php`

`sudo vim config.php `

`sudo service apache2 restart`

![Screenshot 2023-07-15 at 11.27.46](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 11.27.46.png)



![Screenshot 2023-07-15 at 11.57.38](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 11.57.38.png)



![Screenshot 2023-07-15 at 10.40.11](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.40.11.png)

![Screenshot 2023-07-15 at 10.42.00](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 10.42.00.png)

![Screenshot 2023-07-15 at 12.13.18](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 12.13.18.png)

#### Environment Checks

This will indicate if any elements required to run moodle haven't been installed.

![Screenshot 2023-07-15 at 12.13.30](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 12.13.30.png)

![Screenshot 2023-07-15 at 12.14.18](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 12.14.18.png)

![Screenshot 2023-07-15 at 12.16.54](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 12.16.54.png)

![Screenshot 2023-07-15 at 12.17.02](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 12.17.02.png)

![Screenshot 2023-07-15 at 12.18.32](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 12.18.32.png)

username: admin

password:CScs123456!

![Screenshot 2023-07-15 at 12.34.04](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 12.34.04.png)

![Screenshot 2023-07-15 at 12.36.13](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 12.36.13.png)

![Screenshot 2023-07-15 at 12.36.39](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 12.36.39.png)

![Screenshot 2023-07-15 at 12.36.51](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 12.36.51.png)







username: admin

password: CScs123456!



## Student Self Register 

![Screenshot 2023-07-15 at 16.09.32](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.09.32.png)

![Screenshot 2023-07-15 at 16.10.04](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.10.04.png)

![Screenshot 2023-07-15 at 16.11.46](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.11.46.png)

![Screenshot 2023-07-15 at 16.14.03](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.14.03.png)

![Screenshot 2023-07-15 at 16.17.30](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.17.30.png)



Username:student1

Password:Student1!



![Screenshot 2023-07-15 at 16.20.08](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.20.08.png)

Let admin to comfirm



![Screenshot 2023-07-15 at 16.23.58](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.23.58.png)

Let admin to create a new user.

![Screenshot 2023-07-15 at 16.25.22](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.25.22.png)

Username: student2

password:Student2!



Username: professor1

password: Professor1!



![Screenshot 2023-07-15 at 16.39.29](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.39.29.png)



## Turnitin

https://moodle.org/plugins/mod_turnitintooltwo/versions

![Screenshot 2023-07-15 at 16.47.53](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.47.53.png)

![Screenshot 2023-07-15 at 16.49.16](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.49.16.png)



![Screenshot 2023-07-15 at 16.49.00](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.49.00.png)



![Screenshot 2023-07-15 at 16.49.39](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.49.39.png)

![Screenshot 2023-07-15 at 16.49.55](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.49.55.png)

![Screenshot 2023-07-15 at 16.50.10](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.50.10.png)

![Screenshot 2023-07-15 at 16.57.55](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.57.55.png)



![Screenshot 2023-07-15 at 16.59.24](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 16.59.24.png)

if successful, it show be look like this.

![AI_Report](./Check Your Work (LMS) Set up.assets/AI_Report.png)



## CodeCheck

https://moodle.org/plugins/mod_vpl

![Screenshot 2023-07-15 at 18.57.56](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 18.57.56.png)

https://docs.moodle.org/402/en/File_upload_size

![Screenshot 2023-07-15 at 22.15.39](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.15.39.png)

![Screenshot 2023-07-15 at 22.16.02](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.16.02.png)

![Screenshot 2023-07-15 at 22.16.49](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.16.49.png)

![Screenshot 2023-07-15 at 22.17.20](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.17.20.png)

![Screenshot 2023-07-15 at 22.17.34](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.17.34.png)



![Screenshot 2023-07-15 at 22.18.34](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.18.34.png)



![Screenshot 2023-07-15 at 22.18.49](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.18.49.png)

![Screenshot 2023-07-15 at 22.19.00](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.19.00.png)

![Screenshot 2023-07-15 at 22.19.57](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.19.57.png)

![Screenshot 2023-07-15 at 22.20.11](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.20.11.png)

![Screenshot 2023-07-15 at 22.22.07](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.22.07.png)

![Screenshot 2023-07-15 at 22.35.34](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.35.34.png)

![Screenshot 2023-07-15 at 22.47.56](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.47.56.png)

![Screenshot 2023-07-15 at 22.48.38](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.48.38.png)

![Screenshot 2023-07-15 at 22.49.10](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.49.10.png)

![Screenshot 2023-07-15 at 22.49.30](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.49.30.png)

![Screenshot 2023-07-15 at 22.50.41](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 22.50.41.png)

![Screenshot 2023-07-15 at 23.23.38](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 23.23.38.png)

![Screenshot 2023-07-15 at 23.24.06](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 23.24.06.png)



![Screenshot 2023-07-15 at 23.26.06](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 23.26.06.png)

![Screenshot 2023-07-15 at 23.26.38](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 23.26.38.png)









# Architecuture

![architecture](./Check Your Work (LMS) Set up.assets/architecture.svg)



## Load Balancer

https://www.youtube.com/watch?v=JQP96EjRM98&t=399s

![Screenshot 2023-07-16 at 09.44.25](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 09.44.25.png)

![Screenshot 2023-07-16 at 09.45.17](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 09.45.17.png)



![Screenshot 2023-07-16 at 09.42.46](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 09.42.46.png)

![Screenshot 2023-07-16 at 09.46.00](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 09.46.00.png)

![Screenshot 2023-07-16 at 09.46.16](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 09.46.16.png)

![Screenshot 2023-07-16 at 09.46.32](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 09.46.32.png)

![Screenshot 2023-07-16 at 09.46.59](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 09.46.59.png)

## Route 53

www.checkyourworkgroup.online



![Screenshot 2023-07-15 at 17.42.47](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 17.42.47.png)

![Screenshot 2023-07-15 at 17.43.06](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 17.43.06.png)

![Screenshot 2023-07-15 at 17.43.26](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 17.43.26.png)

![Screenshot 2023-07-15 at 17.46.22](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-15 at 17.46.22.png)



![Screenshot 2023-07-16 at 10.43.27](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 10.43.27.png)



## ACM

![Screenshot 2023-07-16 at 10.51.33](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 10.51.33.png)

![Screenshot 2023-07-16 at 10.52.23](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 10.52.23.png)

![Screenshot 2023-07-16 at 10.55.42](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 10.55.42.png)

![Screenshot 2023-07-16 at 10.57.20](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 10.57.20.png)



## Cloudfront

https://aws.amazon.com/cloudfront/

![product-page-diagram_CloudFront_HIW@2x.bce41151308cd621d71591562f6c98e10fcaa949](./Check Your Work (LMS) Set up.assets/product-page-diagram_CloudFront_HIW@2x.bce41151308cd621d71591562f6c98e10fcaa949.png)



![Screenshot 2023-07-16 at 17.11.43](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 17.11.43.png)

![Screenshot 2023-07-16 at 17.12.30](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 17.12.30.png)

![Screenshot 2023-07-16 at 17.11.30](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 17.11.30.png)



![Screenshot 2023-07-16 at 17.44.47](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 17.44.47.png)

## Auto Scaling group

![Screenshot 2023-07-16 at 17.50.57](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 17.50.57.png)

![Screenshot 2023-07-16 at 17.57.52](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 17.57.52.png)

![Screenshot 2023-07-16 at 17.58.31](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 17.58.31.png)

![Screenshot 2023-07-16 at 17.59.48](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 17.59.48.png)

![Screenshot 2023-07-16 at 18.00.16](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 18.00.16.png)

![Screenshot 2023-07-16 at 18.01.03](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 18.01.03.png)

![Screenshot 2023-07-16 at 18.02.19](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 18.02.19.png)

![Screenshot 2023-07-16 at 22.55.53](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 22.55.53.png)

![Screenshot 2023-07-16 at 22.57.17](./Check Your Work (LMS) Set up.assets/Screenshot 2023-07-16 at 22.57.17.png)

