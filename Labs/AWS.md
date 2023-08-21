

account: evecs7346@gmail.com

password:eve123456



AWS: root account: evecs7346@gmail.com

password: Eve123456!

rootname: evecs7346

`sudo apt install awscli`





Exercise 1.1

https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

If you have `sudo` permissions, you can install the AWS CLI for all users on the computer. We provide the steps in one easy to copy and paste group. See the descriptions of each line in the following steps.

```
$ curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
$ sudo installer -pkg AWSCLIV2.pkg -target /
```

1. Download the file using the `curl` command. The `-o` option specifies the file name that the downloaded package is written to. In this example, the file is written to `AWSCLIV2.pkg` in the current folder.

   ```
   $ curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
   ```

2. Run the standard macOS `installer` program, specifying the downloaded `.pkg` file as the source. Use the `-pkg` parameter to specify the name of the package to install, and the `-target /` parameter for which drive to install the package to. The files are installed to `/usr/local/aws-cli`, and a symlink is automatically created in `/usr/local/bin`. You must include `sudo` on the command to grant write permissions to those folders.

   ```
   $ sudo installer -pkg ./AWSCLIV2.pkg -target /
   ```

   After installation is complete, debug logs are written to `/var/log/install.log`.

3. To verify that the shell can find and run the `aws` command in your `$PATH`, use the following commands.

   ```
   $ which aws
   /usr/local/bin/aws 
   $ aws --version
   aws-cli/2.10.0 Python/3.11.2 Darwin/18.7.0 botocore/2.4.5
   ```

   If the `aws` command cannot be found, you might need to restart your terminal or follow the troubleshooting in [Troubleshooting AWS CLI errors](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-troubleshooting.html).



![Screenshot 2023-06-07 at 23.12.13](./AWS.assets/Screenshot 2023-06-07 at 23.12.13.png)

AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources. With IAM









![Screenshot 2023-06-08 at 01.50.46](./AWS.assets/Screenshot 2023-06-08 at 01.50.46.png)

Create alias for AWS account

![Screenshot 2023-06-08 at 01.51.26](./AWS.assets/Screenshot 2023-06-08 at 01.51.26.png)

![Screenshot 2023-06-08 at 01.52.14](./AWS.assets/Screenshot 2023-06-08 at 01.52.14.png)



![Screenshot 2023-06-08 at 01.53.36](./AWS.assets/Screenshot 2023-06-08 at 01.53.36.png)





![Screenshot 2023-06-08 at 01.54.32](./AWS.assets/Screenshot 2023-06-08 at 01.54.32.png)





![Screenshot 2023-06-08 at 02.12.22](./AWS.assets/Screenshot 2023-06-08 at 02.12.22.png)

https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html?icmpid=docs_iam_console#Using_CreateAccessKey



![Screenshot 2023-06-08 at 02.23.17](./AWS.assets/Screenshot 2023-06-08 at 02.23.17.png)

![Screenshot 2023-06-08 at 02.43.58](./AWS.assets/Screenshot 2023-06-08 at 02.43.58.png)

![Screenshot 2023-06-08 at 02.48.35](./AWS.assets/Screenshot 2023-06-08 at 02.48.35.png)

![Screenshot 2023-06-08 at 02.48.55](./AWS.assets/Screenshot 2023-06-08 at 02.48.55.png)

![Screenshot 2023-06-08 at 02.50.13](./AWS.assets/Screenshot 2023-06-08 at 02.50.13.png)

![Screenshot 2023-06-08 at 02.50.35](./AWS.assets/Screenshot 2023-06-08 at 02.50.35.png)

![Screenshot 2023-06-08 at 02.52.57](./AWS.assets/Screenshot 2023-06-08 at 02.52.57.png)

![Screenshot 2023-06-08 at 02.53.28](./AWS.assets/Screenshot 2023-06-08 at 02.53.28.png)

![Screenshot 2023-06-08 at 02.54.09](./AWS.assets/Screenshot 2023-06-08 at 02.54.09.png)

![Screenshot 2023-06-08 at 02.54.30](./AWS.assets/Screenshot 2023-06-08 at 02.54.30.png)

![Screenshot 2023-06-08 at 02.54.55](./AWS.assets/Screenshot 2023-06-08 at 02.54.55.png)

![Screenshot 2023-06-08 at 03.00.44](./AWS.assets/Screenshot 2023-06-08 at 03.00.44.png)

![Screenshot 2023-06-08 at 03.01.30](./AWS.assets/Screenshot 2023-06-08 at 03.01.30.png)

1. Create bucket

   https://awscli.amazonaws.com/v2/documentation/api/latest/reference/s3api/create-bucket.html

   https://docs.aws.amazon.com/cli/latest/userguide/cli-usage-parameters-quoting-strings.html

   ![Screenshot 2023-06-08 at 04.04.30](./AWS.assets/Screenshot 2023-06-08 at 04.04.30.png)

![Screenshot 2023-06-08 at 04.08.05](./AWS.assets/Screenshot 2023-06-08 at 04.08.05.png)

2. 

![Screenshot 2023-06-08 at 04.09.52](./AWS.assets/Screenshot 2023-06-08 at 04.09.52.png)

3.2

1. In the Amazon S3 Console, select the first S3 bucket we created. Select the **Properties** menu. Click the Edit button in **Bucket Versioning**.

![Screenshot 2023-06-08 at 14.51.07](./AWS.assets/Screenshot 2023-06-08 at 14.51.07.png)

![Screenshot 2023-06-08 at 14.51.17](./AWS.assets/Screenshot 2023-06-08 at 14.51.17.png)



2. Click the enable radio button on **Bucket Versioning**, then click **Save changes**.

   ![Screenshot 2023-06-08 at 14.51.50](./AWS.assets/Screenshot 2023-06-08 at 14.51.50.png)

![Screenshot 2023-06-08 at 14.52.16](./AWS.assets/Screenshot 2023-06-08 at 14.52.16.png)

![Screenshot 2023-06-08 at 14.52.37](./AWS.assets/Screenshot 2023-06-08 at 14.52.37.png)

![Screenshot 2023-06-08 at 15.02.07](../../../Library/Application Support/typora-user-images/Screenshot 2023-06-08 at 15.02.07.png)

2. 

![Screenshot 2023-06-08 at 14.56.28](./AWS.assets/Screenshot 2023-06-08 at 14.56.28.png)

![Screenshot 2023-06-08 at 14.57.58](./AWS.assets/Screenshot 2023-06-08 at 14.57.58.png)

![Screenshot 2023-06-08 at 15.04.36](./AWS.assets/Screenshot 2023-06-08 at 15.04.36.png)

![Screenshot 2023-06-08 at 15.12.27](./AWS.assets/Screenshot 2023-06-08 at 15.12.27.png)



4. step

   ![Screenshot 2023-06-08 at 15.27.40](./AWS.assets/Screenshot 2023-06-08 at 15.27.40.png)

![Screenshot 2023-06-08 at 15.32.03](./AWS.assets/Screenshot 2023-06-08 at 15.34.41.png)

![Screenshot 2023-06-08 at 15.32.45](./AWS.assets/Screenshot 2023-06-08 at 15.32.45.png)



5

![Screenshot 2023-06-08 at 16.28.53](./AWS.assets/Screenshot 2023-06-08 at 16.28.53.png)

![Screenshot 2023-06-08 at 17.13.49](./AWS.assets/Screenshot 2023-06-08 at 17.13.49.png)





6.

![Screenshot 2023-06-08 at 17.19.42](./AWS.assets/Screenshot 2023-06-08 at 17.19.42.png)

![Screenshot 2023-06-08 at 17.19.57](./AWS.assets/Screenshot 2023-06-08 at 17.20.18.png)

![Screenshot 2023-06-08 at 17.21.15](./AWS.assets/Screenshot 2023-06-08 at 17.21.15.png)



3.3

1 

![Screenshot 2023-06-08 at 17.47.22](./AWS.assets/Screenshot 2023-06-08 at 17.47.22.png)

2



![Screenshot 2023-06-08 at 17.48.00](./AWS.assets/Screenshot 2023-06-08 at 17.48.00.png)





3

![Screenshot 2023-06-08 at 19.40.06](./AWS.assets/Screenshot 2023-06-08 at 19.40.06.png)



3.4

![Screenshot 2023-06-08 at 20.16.26](./AWS.assets/Screenshot 2023-06-08 at 20.16.26.png)

![Screenshot 2023-06-08 at 20.33.11](./AWS.assets/Screenshot 2023-06-08 at 20.33.11.png)

![Screenshot 2023-06-08 at 20.33.37](./AWS.assets/Screenshot 2023-06-08 at 20.33.37.png)

2

![Screenshot 2023-06-08 at 20.47.25](./AWS.assets/Screenshot 2023-06-08 at 20.47.25.png)

![Screenshot 2023-06-08 at 22.39.25](./AWS.assets/Screenshot 2023-06-08 at 22.39.25.png)

![Screenshot 2023-06-08 at 22.40.42](./AWS.assets/Screenshot 2023-06-08 at 22.40.42.png)

![Screenshot 2023-06-08 at 22.42.01](./AWS.assets/Screenshot 2023-06-08 at 22.42.01.png)

![Screenshot 2023-06-08 at 22.45.45](./AWS.assets/Screenshot 2023-06-08 at 22.45.45.png)

![Screenshot 2023-06-08 at 22.46.27](./AWS.assets/Screenshot 2023-06-08 at 22.46.27.png)



![Screenshot 2023-06-08 at 22.46.54](./AWS.assets/Screenshot 2023-06-08 at 22.46.54.png)





3.5

![Screenshot 2023-06-11 at 01.15.50](./AWS.assets/Screenshot 2023-06-11 at 01.15.50.png)

https://docs.aws.amazon.com/pricing-calculator/latest/userguide/create-estimate.html

![Screenshot 2023-06-11 at 01.25.31](./AWS.assets/Screenshot 2023-06-11 at 01.25.31.png)

![Screenshot 2023-06-11 at 01.28.17](./AWS.assets/Screenshot 2023-06-11 at 01.28.17.png)

![Screenshot 2023-06-11 at 01.29.23](./AWS.assets/Screenshot 2023-06-11 at 01.29.23.png)



5.1

1

![Screenshot 2023-06-11 at 13.23.59](./AWS.assets/Screenshot 2023-06-11 at 13.23.59.png)

2

![Screenshot 2023-06-11 at 13.24.21](./AWS.assets/Screenshot 2023-06-11 at 13.24.21.png)

3

![Screenshot 2023-06-11 at 13.24.40](./AWS.assets/Screenshot 2023-06-11 at 13.24.40.png)



4

![Screenshot 2023-06-11 at 13.26.28](./AWS.assets/Screenshot 2023-06-11 at 13.26.28.png)

5

![Screenshot 2023-06-11 at 13.26.55](./AWS.assets/Screenshot 2023-06-11 at 13.26.55.png)

6

![Screenshot 2023-06-11 at 13.28.32](./AWS.assets/Screenshot 2023-06-11 at 13.28.32.png)

username: admin

password: eve123456



7

![Screenshot 2023-06-11 at 13.31.18](./AWS.assets/Screenshot 2023-06-11 at 13.31.18.png)

8

![Screenshot 2023-06-11 at 13.30.36](./AWS.assets/Screenshot 2023-06-11 at 13.30.36.png)



9

![Screenshot 2023-06-11 at 13.32.06](./AWS.assets/Screenshot 2023-06-11 at 13.32.06.png)

![Screenshot 2023-06-11 at 14.03.57](./AWS.assets/Screenshot 2023-06-11 at 14.03.57.png)





5.2

1

![Screenshot 2023-06-11 at 14.04.44](./AWS.assets/Screenshot 2023-06-11 at 14.04.44.png)





2



![Screenshot 2023-06-11 at 14.05.09](./AWS.assets/Screenshot 2023-06-11 at 14.05.09.png)

3



![Screenshot 2023-06-11 at 14.06.48](./AWS.assets/Screenshot 2023-06-11 at 14.06.48.png)

4



![Screenshot 2023-06-11 at 14.07.07](./AWS.assets/Screenshot 2023-06-11 at 14.07.07.png)





5.3

1

![Screenshot 2023-06-11 at 14.14.45](./AWS.assets/Screenshot 2023-06-11 at 14.14.45.png)

2

![Screenshot 2023-06-11 at 14.15.17](./AWS.assets/Screenshot 2023-06-11 at 14.15.17.png)

3

![Screenshot 2023-06-11 at 14.15.58](./AWS.assets/Screenshot 2023-06-11 at 14.15.58.png)

4

![Screenshot 2023-06-11 at 14.16.33](./AWS.assets/Screenshot 2023-06-11 at 14.16.33.png)

5

![Screenshot 2023-06-11 at 14.16.46](./AWS.assets/Screenshot 2023-06-11 at 14.16.46.png)





5.4

1

![Screenshot 2023-06-11 at 15.30.59](./AWS.assets/Screenshot 2023-06-11 at 15.30.59.png)

2

![Screenshot 2023-06-11 at 15.32.58](./AWS.assets/Screenshot 2023-06-11 at 15.32.58.png)





6.1

![Screenshot 2023-06-14 at 16.46.30](./AWS.assets/Screenshot 2023-06-14 at 16.46.30.png)

1

![Screenshot 2023-06-14 at 16.40.04](./AWS.assets/Screenshot 2023-06-14 at 16.40.04.png)

![Screenshot 2023-06-14 at 16.40.46](./AWS.assets/Screenshot 2023-06-14 at 16.40.46.png)

![Screenshot 2023-06-14 at 16.42.54](./AWS.assets/Screenshot 2023-06-14 at 16.42.54.png)

![Screenshot 2023-06-14 at 16.43.12](./AWS.assets/Screenshot 2023-06-14 at 16.43.12.png)

![Screenshot 2023-06-14 at 16.43.30](./AWS.assets/Screenshot 2023-06-14 at 16.43.30.png)

![Screenshot 2023-06-14 at 16.44.08](./AWS.assets/Screenshot 2023-06-14 at 16.44.08.png)

2

![Screenshot 2023-06-14 at 16.45.41](./AWS.assets/Screenshot 2023-06-14 at 16.45.41.png)



3



![Screenshot 2023-06-14 at 16.47.56](./AWS.assets/Screenshot 2023-06-14 at 16.47.56.png)

4

![Screenshot 2023-06-14 at 17.10.18](./AWS.assets/Screenshot 2023-06-14 at 17.10.18.png)

![Screenshot 2023-06-14 at 17.09.30](./AWS.assets/Screenshot 2023-06-14 at 17.09.30.png)

![sa](./AWS.assets/Screenshot 2023-06-14 at 17.08.08.png)



![Screenshot 2023-06-14 at 17.07.55](./AWS.assets/Screenshot 2023-06-14 at 17.07.55.png)

![Screenshot 2023-06-14 at 17.12.12](./AWS.assets/Screenshot 2023-06-14 at 17.12.12.png)

New password: Eve1234567!



5



![Screenshot 2023-06-14 at 17.13.01](./AWS.assets/Screenshot 2023-06-14 at 17.13.01.png)





![Screenshot 2023-06-14 at 17.15.02](./AWS.assets/Screenshot 2023-06-14 at 17.15.02.png)





6.2

1 

![Screenshot 2023-06-14 at 17.17.42](./AWS.assets/Screenshot 2023-06-14 at 17.17.42.png)

![Screenshot 2023-06-14 at 17.18.03](./AWS.assets/Screenshot 2023-06-14 at 17.18.03.png)



2



![Screenshot 2023-06-14 at 17.22.17](./AWS.assets/Screenshot 2023-06-14 at 17.22.17.png)

![Screenshot 2023-06-14 at 17.23.11](./AWS.assets/Screenshot 2023-06-14 at 17.23.11.png)



![Screenshot 2023-06-17 at 00.38.32](./AWS.assets/Screenshot 2023-06-17 at 00.38.32.png)

3

![Screenshot 2023-06-17 at 00.49.19](./AWS.assets/Screenshot 2023-06-17 at 00.49.19.png)

![Screenshot 2023-06-17 at 00.50.18](./AWS.assets/Screenshot 2023-06-17 at 00.50.18.png)

![Screenshot 2023-06-17 at 00.50.34](./AWS.assets/Screenshot 2023-06-17 at 00.50.34.png)

4

![Screenshot 2023-06-17 at 00.51.39](./AWS.assets/Screenshot 2023-06-17 at 00.51.39.png)

![Screenshot 2023-06-17 at 00.52.30](./AWS.assets/Screenshot 2023-06-17 at 00.52.30.png)

![Screenshot 2023-06-17 at 00.53.44](./AWS.assets/Screenshot 2023-06-17 at 00.53.44.png)

![Screenshot 2023-06-17 at 00.53.56](./AWS.assets/Screenshot 2023-06-17 at 00.53.56.png)

5

![Screenshot 2023-06-17 at 00.55.12](./AWS.assets/Screenshot 2023-06-17 at 00.55.12.png)

![Screenshot 2023-06-17 at 00.56.06](./AWS.assets/Screenshot 2023-06-17 at 00.56.06.png)

![Screenshot 2023-06-17 at 00.57.02](./AWS.assets/Screenshot 2023-06-17 at 00.57.02.png)







6.3

![Screenshot 2023-06-17 at 01.30.12](./AWS.assets/Screenshot 2023-06-17 at 01.30.12.png)

1

![Screenshot 2023-06-18 at 10.29.10](./AWS.assets/Screenshot 2023-06-18 at 10.29.10.png)



![Screenshot 2023-06-18 at 10.30.04](./AWS.assets/Screenshot 2023-06-18 at 10.30.04.png)

![Screenshot 2023-06-18 at 10.31.07](./AWS.assets/Screenshot 2023-06-18 at 10.31.07.png)

![Screenshot 2023-06-18 at 10.31.44](./AWS.assets/Screenshot 2023-06-18 at 10.31.44.png)

![Screenshot 2023-06-18 at 10.32.04](./AWS.assets/Screenshot 2023-06-18 at 10.32.04.png)

2

![Screenshot 2023-06-18 at 10.36.01](./AWS.assets/Screenshot 2023-06-18 at 10.36.01.png)

![Screenshot 2023-06-18 at 10.36.53](./AWS.assets/Screenshot 2023-06-18 at 10.36.53.png)

![Screenshot 2023-06-18 at 11.42.34](./AWS.assets/Screenshot 2023-06-18 at 11.42.34.png)

3

![Screenshot 2023-06-18 at 11.43.34](./AWS.assets/Screenshot 2023-06-18 at 11.43.34.png)



![Screenshot 2023-06-18 at 12.05.15](./AWS.assets/Screenshot 2023-06-18 at 12.05.15.png)



![Screenshot 2023-06-18 at 12.08.51](./AWS.assets/Screenshot 2023-06-18 at 12.08.51.png)

4



![Screenshot 2023-06-18 at 12.24.06](./AWS.assets/Screenshot 2023-06-18 at 12.24.06.png)

![Screenshot 2023-06-18 at 12.24.16](./AWS.assets/Screenshot 2023-06-18 at 12.24.16.png)

![Screenshot 2023-06-18 at 12.24.30](./AWS.assets/Screenshot 2023-06-18 at 12.24.30.png)



5

![Screenshot 2023-06-18 at 12.25.13](./AWS.assets/Screenshot 2023-06-18 at 12.25.13.png)



6.4 

![Screenshot 2023-06-18 at 12.45.42](./AWS.assets/Screenshot 2023-06-18 at 12.45.42.png)

1

create user1 and user2

![Screenshot 2023-06-18 at 12.49.22](./AWS.assets/Screenshot 2023-06-18 at 12.49.22.png)

2

![Screenshot 2023-06-18 at 12.52.27](./AWS.assets/Screenshot 2023-06-18 at 12.52.27.png)

3

![Screenshot 2023-06-18 at 12.52.51](./AWS.assets/Screenshot 2023-06-18 at 12.52.51.png)

4

![Screenshot 2023-06-18 at 12.55.27](./AWS.assets/Screenshot 2023-06-18 at 12.55.27.png)

![Screenshot 2023-06-18 at 12.55.54](./AWS.assets/Screenshot 2023-06-18 at 12.55.54.png)

![Screenshot 2023-06-18 at 12.56.50](./AWS.assets/Screenshot 2023-06-18 at 12.56.50.png)



![Screenshot 2023-06-18 at 12.57.03](./AWS.assets/Screenshot 2023-06-18 at 12.57.03.png)

![Screenshot 2023-06-18 at 12.58.13](./AWS.assets/Screenshot 2023-06-18 at 12.58.13.png)

![Screenshot 2023-06-18 at 12.58.29](./AWS.assets/Screenshot 2023-06-18 at 12.58.29.png)







![Screenshot 2023-06-18 at 13.06.48](./AWS.assets/Screenshot 2023-06-18 at 13.06.48.png)

![Screenshot 2023-06-18 at 13.07.11](./AWS.assets/Screenshot 2023-06-18 at 13.07.11.png)

5

![Screenshot 2023-06-18 at 13.10.59](./AWS.assets/Screenshot 2023-06-18 at 13.10.59.png)

![Screenshot 2023-06-18 at 13.11.20](./AWS.assets/Screenshot 2023-06-18 at 13.11.20.png)

![Screenshot 2023-06-18 at 13.11.32](./AWS.assets/Screenshot 2023-06-18 at 13.11.32.png)

![Screenshot 2023-06-18 at 13.13.07](./AWS.assets/Screenshot 2023-06-18 at 13.13.07.png)

![Screenshot 2023-06-18 at 13.17.50](./AWS.assets/Screenshot 2023-06-18 at 13.17.50.png)

![Screenshot 2023-06-18 at 13.18.31](./AWS.assets/Screenshot 2023-06-18 at 13.18.31.png)

![Screenshot 2023-06-18 at 13.18.40](../../../Library/Application Support/typora-user-images/Screenshot 2023-06-18 at 13.18.40.png)









# 2

2.1



![Screenshot 2023-06-27 at 01.04.25](./AWS.assets/Screenshot 2023-06-27 at 01.04.25.png)

![Screenshot 2023-06-27 at 01.04.59](./AWS.assets/Screenshot 2023-06-27 at 01.04.59.png)



1

![Screenshot 2023-06-27 at 01.20.42](./AWS.assets/Screenshot 2023-06-27 at 01.20.42.png)

![Screenshot 2023-06-27 at 01.23.02](./AWS.assets/Screenshot 2023-06-27 at 01.23.02.png)

![Screenshot 2023-06-27 at 01.23.25](./AWS.assets/Screenshot 2023-06-27 at 01.23.25.png)



2 

![Screenshot 2023-06-27 at 01.28.28](./AWS.assets/Screenshot 2023-06-27 at 01.28.28.png)

![Screenshot 2023-06-27 at 01.28.50](./AWS.assets/Screenshot 2023-06-27 at 01.28.50.png)



3

![Screenshot 2023-06-27 at 01.31.22](./AWS.assets/Screenshot 2023-06-27 at 01.31.22.png)

4 

![Screenshot 2023-06-27 at 01.32.23](./AWS.assets/Screenshot 2023-06-27 at 01.32.23.png)

![Screenshot 2023-06-27 at 01.32.38](./AWS.assets/Screenshot 2023-06-27 at 01.32.38.png)



5 

![Screenshot 2023-06-27 at 01.33.44](./AWS.assets/Screenshot 2023-06-27 at 01.33.44.png)



![Screenshot 2023-06-27 at 01.36.42](./AWS.assets/Screenshot 2023-06-27 at 01.36.42.png)

6 

![Screenshot 2023-06-27 at 01.37.27](./AWS.assets/Screenshot 2023-06-27 at 01.37.27.png)



![Screenshot 2023-06-27 at 01.38.13](./AWS.assets/Screenshot 2023-06-27 at 01.38.13.png)

![Screenshot 2023-06-27 at 01.58.43](./AWS.assets/Screenshot 2023-06-27 at 01.58.43.png)

![Screenshot 2023-06-27 at 01.58.58](./AWS.assets/Screenshot 2023-06-27 at 01.58.58.png)





2.2



![Screenshot 2023-06-27 at 01.05.43](./AWS.assets/Screenshot 2023-06-27 at 01.05.43.png)

1

![Screenshot 2023-06-27 at 02.01.23](./AWS.assets/Screenshot 2023-06-27 at 02.01.23.png)

2 

![Screenshot 2023-06-27 at 02.03.03](./AWS.assets/Screenshot 2023-06-27 at 02.03.03.png)

![Screenshot 2023-06-27 at 02.03.29](./AWS.assets/Screenshot 2023-06-27 at 02.03.29.png)

![Screenshot 2023-06-27 at 02.03.47](./AWS.assets/Screenshot 2023-06-27 at 02.03.47.png)

![Screenshot 2023-06-27 at 02.04.41](./AWS.assets/Screenshot 2023-06-27 at 02.04.41.png)



3 

![Screenshot 2023-06-27 at 02.05.23](./AWS.assets/Screenshot 2023-06-27 at 02.05.23.png)

![Screenshot 2023-06-27 at 02.07.13](./AWS.assets/Screenshot 2023-06-27 at 02.07.13.png)

![Screenshot 2023-06-27 at 02.07.29](./AWS.assets/Screenshot 2023-06-27 at 02.07.29.png)

![Screenshot 2023-06-27 at 02.08.48](./AWS.assets/Screenshot 2023-06-27 at 02.08.48.png)



2.3

![Screenshot 2023-06-27 at 02.08.26](./AWS.assets/Screenshot 2023-06-27 at 02.08.26.png)

https://aws.amazon.com/ec2/instance-types/f1/

![Screenshot 2023-06-27 at 08.46.07](./AWS.assets/Screenshot 2023-06-27 at 08.46.07.png)

on-demand model: 100 hours: 1.65 * 100   = 165 $

reserved instance 1 year:   1.06 * 365 * 24 = 9285.6

month: 165 /12 = 13.75 $ 

year: 165 $



reserved instance 1 year:   1.06 * 365 * 24 = 9285.6

month:  9285.6/12 = 773.8000000000001



2.4 

![Screenshot 2023-06-27 at 02.19.10](./AWS.assets/Screenshot 2023-06-27 at 02.19.10.png)

1 

![Screenshot 2023-06-27 at 09.39.49](./AWS.assets/Screenshot 2023-06-27 at 09.39.49.png)

![Screenshot 2023-06-27 at 09.41.30](./AWS.assets/Screenshot 2023-06-27 at 09.41.30.png)



![Screenshot 2023-06-27 at 09.42.07](./AWS.assets/Screenshot 2023-06-27 at 09.42.07.png)

2 

![Screenshot 2023-06-27 at 09.43.44](./AWS.assets/Screenshot 2023-06-27 at 09.43.44.png)

![Screenshot 2023-06-27 at 09.45.17](./AWS.assets/Screenshot 2023-06-27 at 09.45.17.png)

![Screenshot 2023-06-27 at 09.46.08](./AWS.assets/Screenshot 2023-06-27 at 09.46.08.png)

3 

![Screenshot 2023-06-27 at 10.57.32](./AWS.assets/Screenshot 2023-06-27 at 10.57.32.png)

![Screenshot 2023-06-27 at 10.58.25](./AWS.assets/Screenshot 2023-06-27 at 10.58.25.png)

4 

![Screenshot 2023-06-27 at 11.02.19](./AWS.assets/Screenshot 2023-06-27 at 11.02.19.png)

![Screenshot 2023-06-27 at 11.08.31](./AWS.assets/Screenshot 2023-06-27 at 11.08.31.png)

2.5

![Screenshot 2023-06-27 at 02.19.33](./AWS.assets/Screenshot 2023-06-27 at 02.19.33.png)

1 

![Screenshot 2023-06-27 at 11.24.42](./AWS.assets/Screenshot 2023-06-27 at 11.24.42.png)



2

![Screenshot 2023-06-27 at 11.25.04](./AWS.assets/Screenshot 2023-06-27 at 11.25.04.png)

3

![Screenshot 2023-06-27 at 11.25.39](./AWS.assets/Screenshot 2023-06-27 at 11.25.39.png)

4

![Screenshot 2023-06-27 at 11.48.55](./AWS.assets/Screenshot 2023-06-27 at 11.48.55.png)

![Screenshot 2023-06-27 at 11.49.36](./AWS.assets/Screenshot 2023-06-27 at 11.49.36.png)

5

![Screenshot 2023-06-27 at 11.50.07](./AWS.assets/Screenshot 2023-06-27 at 11.50.07.png)

6  ![Screenshot 2023-06-27 at 11.59.17](./AWS.assets/Screenshot 2023-06-27 at 11.59.17.png)

7

![Screenshot 2023-06-27 at 12.00.42](./AWS.assets/Screenshot 2023-06-27 at 12.00.42.png)



8

![Screenshot 2023-06-27 at 12.01.06](./AWS.assets/Screenshot 2023-06-27 at 12.01.06.png)

9

![Screenshot 2023-06-27 at 12.03.18](./AWS.assets/Screenshot 2023-06-27 at 12.03.18.png)

10

![Screenshot 2023-06-27 at 12.04.11](./AWS.assets/Screenshot 2023-06-27 at 12.04.11.png)

11

![Screenshot 2023-06-27 at 12.05.38](./AWS.assets/Screenshot 2023-06-27 at 12.05.38.png)

12 

![Screenshot 2023-06-27 at 12.09.29](./AWS.assets/Screenshot 2023-06-27 at 12.09.29.png)

![Screenshot 2023-06-27 at 12.25.40](./AWS.assets/Screenshot 2023-06-27 at 12.25.40.png)



1

![Screenshot 2023-06-27 at 13.51.20](./AWS.assets/Screenshot 2023-06-27 at 13.51.20.png)

2

![Screenshot 2023-06-27 at 13.48.21](./AWS.assets/Screenshot 2023-06-27 at 13.48.21.png)



3

![Screenshot 2023-06-27 at 13.50.11](./AWS.assets/Screenshot 2023-06-27 at 13.50.11.png)

4

![Screenshot 2023-06-27 at 13.55.14](./AWS.assets/Screenshot 2023-06-27 at 13.55.14.png)

5 ![Screenshot 2023-06-27 at 13.55.49](./AWS.assets/Screenshot 2023-06-27 at 13.55.49.png)

![Screenshot 2023-06-27 at 13.58.22](./AWS.assets/Screenshot 2023-06-27 at 13.58.22.png)



7

![Screenshot 2023-06-27 at 14.01.10](./AWS.assets/Screenshot 2023-06-27 at 14.01.10.png)

8

![Screenshot 2023-06-27 at 14.02.07](./AWS.assets/Screenshot 2023-06-27 at 14.02.07.png)



![Screenshot 2023-06-27 at 14.04.22](./AWS.assets/Screenshot 2023-06-27 at 14.04.22.png)

9

![Screenshot 2023-06-27 at 14.05.18](./AWS.assets/Screenshot 2023-06-27 at 14.05.18.png)

10

![Screenshot 2023-06-27 at 14.06.02](./AWS.assets/Screenshot 2023-06-27 at 14.06.02.png)

11

![Screenshot 2023-06-27 at 14.07.53](./AWS.assets/Screenshot 2023-06-27 at 14.07.53.png)



![Screenshot 2023-06-27 at 14.51.22](./AWS.assets/Screenshot 2023-06-27 at 14.51.22.png)

![Screenshot 2023-06-27 at 14.52.56](./AWS.assets/Screenshot 2023-06-27 at 14.52.56.png)

![Screenshot 2023-06-27 at 16.00.23](./AWS.assets/Screenshot 2023-06-27 at 16.00.23.png)

![Screenshot 2023-06-27 at 15.54.11](./AWS.assets/Screenshot 2023-06-27 at 15.54.11.png)

https://cloudkatha.com/how-to-install-apache-2-on-aws-ec2-instance-ubuntu-20-04/



2.6

![Screenshot 2023-06-27 at 02.19.59](./AWS.assets/Screenshot 2023-06-27 at 02.19.59.png)

![Screenshot 2023-06-27 at 16.28.13](./AWS.assets/Screenshot 2023-06-27 at 16.28.13.png)

2.7

![Screenshot 2023-06-27 at 02.20.21](./AWS.assets/Screenshot 2023-06-27 at 02.20.21.png)



![Screenshot 2023-06-27 at 16.31.02](./AWS.assets/Screenshot 2023-06-27 at 16.31.02.png)





## Chapter 4 Amazon Virtual Private Cloud (VPC)

### Exercise 4.1

![Screenshot 2023-07-04 at 01.15.58](./AWS.assets/Screenshot 2023-07-04 at 01.15.58.png)

![Screenshot 2023-07-04 at 01.16.31](./AWS.assets/Screenshot 2023-07-04 at 01.16.31.png)

![Screenshot 2023-07-04 at 01.48.21](./AWS.assets/Screenshot 2023-07-04 at 01.48.21.png)

![Screenshot 2023-07-04 at 01.47.50](./AWS.assets/Screenshot 2023-07-04 at 01.47.50.png)

![Screenshot 2023-07-04 at 01.53.03](./AWS.assets/Screenshot 2023-07-04 at 01.53.03.png)

![Screenshot 2023-07-04 at 01.51.56](./AWS.assets/Screenshot 2023-07-04 at 01.51.56.png)

![Screenshot 2023-07-04 at 02.02.56](./AWS.assets/Screenshot 2023-07-04 at 02.02.56.png)

### Exercise 4.2

![Screenshot 2023-07-04 at 09.58.10](./AWS.assets/Screenshot 2023-07-04 at 09.58.10.png)

![Screenshot 2023-07-04 at 09.58.50](./AWS.assets/Screenshot 2023-07-04 at 09.58.50.png)

![](./AWS.assets/Screenshot 2023-07-04 at 10.04.16.png)

![Screenshot 2023-07-04 at 10.03.41](./AWS.assets/Screenshot 2023-07-04 at 10.03.41.png)

![Screenshot 2023-07-04 at 10.05.06](./AWS.assets/Screenshot 2023-07-04 at 10.05.06.png)

![Screenshot 2023-07-04 at 10.05.20](./AWS.assets/Screenshot 2023-07-04 at 10.05.20.png)

![Screenshot 2023-07-04 at 10.07.01](./AWS.assets/Screenshot 2023-07-04 at 10.07.01.png)

### Exercise 4.3

![Screenshot 2023-07-04 at 11.17.06](./AWS.assets/Screenshot 2023-07-04 at 11.17.06.png)

![Screenshot 2023-07-04 at 11.17.24](./AWS.assets/Screenshot 2023-07-04 at 11.17.24.png)

![Screenshot 2023-07-04 at 11.25.12](./AWS.assets/Screenshot 2023-07-04 at 11.25.12.png)

![Screenshot 2023-07-04 at 11.26.36](./AWS.assets/Screenshot 2023-07-04 at 11.26.36.png)

![Screenshot 2023-07-04 at 11.26.47](./AWS.assets/Screenshot 2023-07-04 at 11.26.47.png)

### Exercise 4.4

![Screenshot 2023-07-04 at 11.40.05](./AWS.assets/Screenshot 2023-07-04 at 11.40.05.png)

![Screenshot 2023-07-04 at 11.41.55](./AWS.assets/Screenshot 2023-07-04 at 11.41.55.png)

![Screenshot 2023-07-04 at 11.42.12](./AWS.assets/Screenshot 2023-07-04 at 11.42.12.png)

1

![Screenshot 2023-07-04 at 11.43.46](./AWS.assets/Screenshot 2023-07-04 at 11.43.46.png)

2

![Screenshot 2023-07-04 at 11.46.25](./AWS.assets/Screenshot 2023-07-04 at 11.46.25.png)

3 

![Screenshot 2023-07-04 at 11.47.48](./AWS.assets/Screenshot 2023-07-04 at 11.47.48.png)

4 

![Screenshot 2023-07-04 at 11.51.49](./AWS.assets/Screenshot 2023-07-04 at 11.51.49.png)

5

![Screenshot 2023-07-04 at 11.53.08](./AWS.assets/Screenshot 2023-07-04 at 11.53.08.png)



### Exercise 4.5

![Screenshot 2023-07-04 at 12.07.33](./AWS.assets/Screenshot 2023-07-04 at 12.07.33.png)

![Screenshot 2023-07-04 at 12.07.47](./AWS.assets/Screenshot 2023-07-04 at 12.07.47.png)

1

![Screenshot 2023-07-04 at 12.28.17](./AWS.assets/Screenshot 2023-07-04 at 12.28.17.png)

2 

![Screenshot 2023-07-04 at 12.30.41](./AWS.assets/Screenshot 2023-07-04 at 12.30.41.png)

![Screenshot 2023-07-04 at 12.31.12](./AWS.assets/Screenshot 2023-07-04 at 12.31.12.png)

![Screenshot 2023-07-04 at 12.31.20](./AWS.assets/Screenshot 2023-07-04 at 12.31.20.png)



3 

![Screenshot 2023-07-04 at 12.33.25](./AWS.assets/Screenshot 2023-07-04 at 12.33.25.png)

### Exercise 4.6

![Screenshot 2023-07-04 at 14.51.22](./AWS.assets/Screenshot 2023-07-04 at 14.51.22.png)

![Screenshot 2023-07-04 at 14.51.57](./AWS.assets/Screenshot 2023-07-04 at 14.51.57.png)



1

![Screenshot 2023-07-04 at 14.50.56](./AWS.assets/Screenshot 2023-07-04 at 14.50.56.png)

2

![Screenshot 2023-07-04 at 14.58.23](./AWS.assets/Screenshot 2023-07-04 at 14.58.23.png)

3

![Screenshot 2023-07-04 at 15.43.33](./AWS.assets/Screenshot 2023-07-04 at 15.43.33.png)

4

![Screenshot 2023-07-04 at 15.50.02](./AWS.assets/Screenshot 2023-07-04 at 15.50.02.png)

![Screenshot 2023-07-04 at 15.48.58](./AWS.assets/Screenshot 2023-07-04 at 15.48.58.png)

### Exercise 4.7

![Screenshot 2023-07-04 at 16.12.04](./AWS.assets/Screenshot 2023-07-04 at 16.12.04.png)

<img src="./AWS.assets/Screenshot 2023-07-04 at 16.12.18.png" alt="Screenshot 2023-07-04 at 16.12.18" style="zoom: 50%;" />

![Screenshot 2023-07-04 at 16.12.43](./AWS.assets/Screenshot 2023-07-04 at 16.12.43.png)

1

![Screenshot 2023-07-04 at 16.13.28](./AWS.assets/Screenshot 2023-07-04 at 16.13.28.png)

2 

![Screenshot 2023-07-04 at 16.18.00](./AWS.assets/Screenshot 2023-07-04 at 16.18.00.png)

![Screenshot 2023-07-04 at 16.17.43](./AWS.assets/Screenshot 2023-07-04 at 16.17.43.png)

3

![Screenshot 2023-07-04 at 16.19.46](./AWS.assets/Screenshot 2023-07-04 at 16.19.46.png)

### Exercise 4.8

![Screenshot 2023-07-04 at 16.53.11](./AWS.assets/Screenshot 2023-07-04 at 16.53.11.png)

![Screenshot 2023-07-04 at 16.53.30](./AWS.assets/Screenshot 2023-07-04 at 16.53.30.png)

![Screenshot 2023-07-04 at 16.53.51](./AWS.assets/Screenshot 2023-07-04 at 16.53.51.png)

![Screenshot 2023-07-04 at 16.54.08](./AWS.assets/Screenshot 2023-07-04 at 16.54.08.png)

![Screenshot 2023-07-04 at 16.54.21](./AWS.assets/Screenshot 2023-07-04 at 16.54.21.png)



1 

![Screenshot 2023-07-04 at 16.55.38](./AWS.assets/Screenshot 2023-07-04 at 16.55.38.png)

![Screenshot 2023-07-04 at 16.58.44](./AWS.assets/Screenshot 2023-07-04 at 16.58.44.png)

2 

![Screenshot 2023-07-04 at 16.59.23](./AWS.assets/Screenshot 2023-07-04 at 16.59.23.png)

3 

![Screenshot 2023-07-04 at 17.11.14](./AWS.assets/Screenshot 2023-07-04 at 17.11.14.png)

![Screenshot 2023-07-04 at 17.10.50](./AWS.assets/Screenshot 2023-07-04 at 17.10.50.png)

![Screenshot 2023-07-04 at 17.14.33](./AWS.assets/Screenshot 2023-07-04 at 17.14.33.png)

![Screenshot 2023-07-04 at 17.15.34](./AWS.assets/Screenshot 2023-07-04 at 17.15.34.png)

4

![Screenshot 2023-07-04 at 17.19.18](./AWS.assets/Screenshot 2023-07-04 at 17.19.18.png)

5

![Screenshot 2023-07-04 at 17.33.13](./AWS.assets/Screenshot 2023-07-04 at 17.33.13.png)

![Screenshot 2023-07-04 at 17.31.52](./AWS.assets/Screenshot 2023-07-04 at 17.31.52.png)

![Screenshot 2023-07-04 at 17.33.04](./AWS.assets/Screenshot 2023-07-04 at 17.33.04.png)

6

![Screenshot 2023-07-04 at 17.35.08](./AWS.assets/Screenshot 2023-07-04 at 17.35.08.png)

### Exercise 4.9

![Screenshot 2023-07-04 at 17.54.07](./AWS.assets/Screenshot 2023-07-04 at 17.54.07.png)



1![Screenshot 2023-07-04 at 17.56.06](./AWS.assets/Screenshot 2023-07-04 at 17.56.06.png)

![Screenshot 2023-07-04 at 17.57.34](./AWS.assets/Screenshot 2023-07-04 at 17.57.34.png)

2 

![Screenshot 2023-07-04 at 18.04.59](./AWS.assets/Screenshot 2023-07-04 at 18.04.59.png)

![Screenshot 2023-07-04 at 18.06.10](./AWS.assets/Screenshot 2023-07-04 at 18.06.10.png)

3

![Screenshot 2023-07-04 at 18.07.38](./AWS.assets/Screenshot 2023-07-04 at 18.07.38.png)

![Screenshot 2023-07-04 at 18.07.53](./AWS.assets/Screenshot 2023-07-04 at 18.07.53.png)

## Chapter 7 CloudTrail, CloudWatch, and AWS Config

### Exercise 7.1

![Screenshot 2023-07-10 at 15.51.59](./AWS.assets/Screenshot 2023-07-10 at 15.51.59.png)

1

![Screenshot 2023-07-10 at 17.07.11](./AWS.assets/Screenshot 2023-07-10 at 17.07.11.png)

![Screenshot 2023-07-10 at 17.09.52](./AWS.assets/Screenshot 2023-07-10 at 17.09.52.png)

2

![Screenshot 2023-07-10 at 17.10.56](./AWS.assets/Screenshot 2023-07-10 at 17.10.56.png)

3

![Screenshot 2023-07-10 at 17.11.45](./AWS.assets/Screenshot 2023-07-10 at 17.11.45.png)

4

![Screenshot 2023-07-10 at 17.12.51](./AWS.assets/Screenshot 2023-07-10 at 17.12.51.png)

5

![Screenshot 2023-07-10 at 17.13.40](./AWS.assets/Screenshot 2023-07-10 at 17.13.40.png)



6

![Screenshot 2023-07-10 at 17.20.42](./AWS.assets/Screenshot 2023-07-10 at 17.20.42.png)

7

![Screenshot 2023-07-10 at 17.21.46](./AWS.assets/Screenshot 2023-07-10 at 17.21.46.png)

8

![Screenshot 2023-07-10 at 17.22.01](./AWS.assets/Screenshot 2023-07-10 at 17.22.01.png)

9 

![Screenshot 2023-07-10 at 17.22.24](./AWS.assets/Screenshot 2023-07-10 at 17.22.24.png)

10

![Screenshot 2023-07-10 at 17.22.44](./AWS.assets/Screenshot 2023-07-10 at 17.22.44.png)







### Exercise 7.2

![Screenshot 2023-07-10 at 15.53.26](./AWS.assets/Screenshot 2023-07-10 at 15.53.26.png)



1

![Screenshot 2023-07-10 at 17.40.00](./AWS.assets/Screenshot 2023-07-10 at 17.40.00.png)



2

![Screenshot 2023-07-10 at 17.40.30](./AWS.assets/Screenshot 2023-07-10 at 17.40.30.png)

3

![Screenshot 2023-07-10 at 17.41.51](./AWS.assets/Screenshot 2023-07-10 at 17.41.51.png)

![Screenshot 2023-07-10 at 17.42.08](./AWS.assets/Screenshot 2023-07-10 at 17.42.08.png)

![Screenshot 2023-07-10 at 17.42.35](./AWS.assets/Screenshot 2023-07-10 at 17.42.35.png)

![Screenshot 2023-07-10 at 17.44.44](./AWS.assets/Screenshot 2023-07-10 at 17.44.44.png)

4

![Screenshot 2023-07-10 at 17.45.14](./AWS.assets/Screenshot 2023-07-10 at 17.45.14.png)

5

![Screenshot 2023-07-10 at 17.46.41](./AWS.assets/Screenshot 2023-07-10 at 17.46.41.png)

6

![Screenshot 2023-07-10 at 17.47.36](./AWS.assets/Screenshot 2023-07-10 at 17.47.36.png)

7

![Screenshot 2023-07-10 at 18.30.42](./AWS.assets/Screenshot 2023-07-10 at 18.30.42.png)

8

![Screenshot 2023-07-10 at 17.48.19](./AWS.assets/Screenshot 2023-07-10 at 17.48.19.png)



### Exercise 7.3

![Screenshot 2023-07-10 at 15.52.55](./AWS.assets/Screenshot 2023-07-10 at 15.52.55.png)

1 

![Screenshot 2023-07-10 at 18.43.57](./AWS.assets/Screenshot 2023-07-10 at 18.43.57.png)

2

![Screenshot 2023-07-10 at 18.44.17](./AWS.assets/Screenshot 2023-07-10 at 18.44.17.png)

3

![Screenshot 2023-07-10 at 18.45.14](./AWS.assets/Screenshot 2023-07-10 at 18.45.14.png)

4

![Screenshot 2023-07-10 at 18.46.54](./AWS.assets/Screenshot 2023-07-10 at 18.46.54.png)

5

![Screenshot 2023-07-10 at 18.48.18](./AWS.assets/Screenshot 2023-07-10 at 18.48.18.png)

6

![Screenshot 2023-07-10 at 18.49.40](./AWS.assets/Screenshot 2023-07-10 at 18.49.40.png)

7

![Screenshot 2023-07-10 at 18.50.33](./AWS.assets/Screenshot 2023-07-10 at 18.50.33.png)



## Chapter 8 Amazon Route 53 and CloudFront

### Exercise 8.1

![Screenshot 2023-07-10 at 16.18.04](./AWS.assets/Screenshot 2023-07-10 at 16.18.04.png)



1

![Screenshot 2023-07-11 at 01.06.42](./AWS.assets/Screenshot 2023-07-11 at 01.06.42.png)

![Screenshot 2023-07-11 at 01.07.08](./AWS.assets/Screenshot 2023-07-11 at 01.07.08.png)

2

![Screenshot 2023-07-11 at 18.04.56](./AWS.assets/Screenshot 2023-07-11 at 18.04.56.png)

3

![Screenshot 2023-07-11 at 18.05.23](./AWS.assets/Screenshot 2023-07-11 at 18.05.23.png)

4 

![Screenshot 2023-07-11 at 13.14.12](./AWS.assets/Screenshot 2023-07-11 at 13.14.12.png)





5

![Screenshot 2023-07-11 at 13.15.11](./AWS.assets/Screenshot 2023-07-11 at 13.15.11.png)

![Screenshot 2023-07-11 at 13.17.07](./AWS.assets/Screenshot 2023-07-11 at 13.17.07.png)



![Screenshot 2023-07-11 at 13.18.29](./AWS.assets/Screenshot 2023-07-11 at 13.18.29.png)

![Screenshot 2023-07-11 at 13.18.57](./AWS.assets/Screenshot 2023-07-11 at 13.18.57.png)

6

![Screenshot 2023-07-11 at 13.19.37](./AWS.assets/Screenshot 2023-07-11 at 13.19.37.png)



7

![Screenshot 2023-07-11 at 15.47.03](./AWS.assets/Screenshot 2023-07-11 at 15.47.03.png)

![Screenshot 2023-07-11 at 17.10.22](./AWS.assets/Screenshot 2023-07-11 at 17.10.22.png)

![Screenshot 2023-07-11 at 17.10.48](./AWS.assets/Screenshot 2023-07-11 at 17.10.48.png)

![Screenshot 2023-07-11 at 17.30.55](./AWS.assets/Screenshot 2023-07-11 at 17.30.55.png)

8

![Screenshot 2023-07-11 at 16.03.42](./AWS.assets/Screenshot 2023-07-11 at 16.03.42.png)

9

![Screenshot 2023-07-11 at 17.57.44](./AWS.assets/Screenshot 2023-07-11 at 17.57.44.png)

10

![Screenshot 2023-07-11 at 17.59.48](./AWS.assets/Screenshot 2023-07-11 at 17.59.48.png)



#### Registered domains

https://www.youtube.com/watch?v=JRZiQFVWpi8

![Screenshot 2023-07-11 at 16.14.48](./AWS.assets/Screenshot 2023-07-11 at 16.14.48.png)

![Screenshot 2023-07-11 at 16.15.44](./AWS.assets/Screenshot 2023-07-11 at 16.15.44.png)

![Screenshot 2023-07-11 at 17.42.36](./AWS.assets/Screenshot 2023-07-11 at 17.42.36.png)



![Screenshot 2023-07-11 at 17.42.26](./AWS.assets/Screenshot 2023-07-11 at 17.42.26.png)

9

10



### Exercise 8.2

![Screenshot 2023-07-10 at 16.18.20](./AWS.assets/Screenshot 2023-07-10 at 16.18.20.png)

1

![Screenshot 2023-07-11 at 18.20.14](./AWS.assets/Screenshot 2023-07-11 at 18.20.14.png)



2

![Screenshot 2023-07-11 at 18.22.33](./AWS.assets/Screenshot 2023-07-11 at 18.22.33.png)

3![Screenshot 2023-07-11 at 18.24.08](./AWS.assets/Screenshot 2023-07-11 at 18.24.08.png)

4 

![Screenshot 2023-07-11 at 18.24.08](./AWS.assets/Screenshot 2023-07-11 at 18.24.08.png)

5

![Screenshot 2023-07-11 at 21.16.36](./AWS.assets/Screenshot 2023-07-11 at 21.16.36.png)

![Screenshot 2023-07-11 at 21.09.21](./AWS.assets/Screenshot 2023-07-11 at 21.09.21.png)







6

![Screenshot 2023-07-11 at 21.15.14](./AWS.assets/Screenshot 2023-07-11 at 21.15.14.png)

![Screenshot 2023-07-11 at 21.17.03](./AWS.assets/Screenshot 2023-07-11 at 21.17.03.png)





### Exercise 8.3

![Screenshot 2023-07-10 at 16.18.51](./AWS.assets/Screenshot 2023-07-10 at 16.18.51.png)

--------------------------

![Screenshot 2023-07-12 at 12.04.31](./AWS.assets/Screenshot 2023-07-12 at 12.04.31.png)

![Screenshot 2023-07-12 at 13.56.20](./AWS.assets/Screenshot 2023-07-12 at 13.56.20.png)

![Screenshot 2023-07-12 at 13.57.25](./AWS.assets/Screenshot 2023-07-12 at 13.57.25.png)



![Screenshot 2023-07-12 at 23.14.03](./AWS.assets/Screenshot 2023-07-12 at 23.14.03.png)



![Screenshot 2023-07-12 at 23.14.06](./AWS.assets/Screenshot 2023-07-12 at 23.14.06.png)

![Screenshot 2023-07-12 at 23.17.01](./AWS.assets/Screenshot 2023-07-12 at 23.17.01.png)

![Screenshot 2023-07-12 at 23.21.25](./AWS.assets/Screenshot 2023-07-12 at 23.21.25.png)



![Screenshot 2023-07-12 at 23.23.35](./AWS.assets/Screenshot 2023-07-12 at 23.23.35.png)

---------------

1

![Screenshot 2023-07-14 at 01.38.27](./AWS.assets/Screenshot 2023-07-14 at 01.38.27.png)

![Screenshot 2023-07-14 at 01.44.43](./AWS.assets/Screenshot 2023-07-14 at 01.44.43.png)

![Screenshot 2023-07-13 at 16.10.49](./AWS.assets/Screenshot 2023-07-13 at 16.10.49.png)

2

![Screenshot 2023-07-14 at 00.48.26](./AWS.assets/Screenshot 2023-07-14 at 00.48.26.png)



3 

![Screenshot 2023-07-14 at 01.46.56](./AWS.assets/Screenshot 2023-07-14 at 01.46.56.png)

![Screenshot 2023-07-14 at 00.53.04](./AWS.assets/Screenshot 2023-07-14 at 00.53.04.png)





![Screenshot 2023-07-13 at 16.48.32](./AWS.assets/Screenshot 2023-07-13 at 16.48.32.png)

![Screenshot 2023-07-13 at 16.50.17](./AWS.assets/Screenshot 2023-07-13 at 16.50.17.png)

![Screenshot 2023-07-13 at 16.56.33](./AWS.assets/Screenshot 2023-07-13 at 16.56.33.png)

4

![Screenshot 2023-07-14 at 01.48.35](./AWS.assets/Screenshot 2023-07-14 at 01.48.35.png)

![Screenshot 2023-07-14 at 01.50.11](./AWS.assets/Screenshot 2023-07-14 at 01.50.11.png)





![Screenshot 2023-07-14 at 00.59.44](./AWS.assets/Screenshot 2023-07-14 at 00.59.44.png)

![Screenshot 2023-07-14 at 01.07.43](./AWS.assets/Screenshot 2023-07-14 at 01.07.43.png)

![Screenshot 2023-07-13 at 17.00.59](./AWS.assets/Screenshot 2023-07-13 at 17.00.59.png)

5

![Screenshot 2023-07-14 at 01.02.37](./AWS.assets/Screenshot 2023-07-14 at 01.02.37.png)

![Screenshot 2023-07-14 at 01.06.00](./AWS.assets/Screenshot 2023-07-14 at 01.06.00.png)

![Screenshot 2023-07-14 at 01.10.21](./AWS.assets/Screenshot 2023-07-14 at 01.10.21.png)



![Screenshot 2023-07-13 at 17.02.37](./AWS.assets/Screenshot 2023-07-13 at 17.02.37.png)



6

![Screenshot 2023-07-14 at 01.15.57](./AWS.assets/Screenshot 2023-07-14 at 01.15.57.png)

![Screenshot 2023-07-14 at 01.12.24](./AWS.assets/Screenshot 2023-07-14 at 01.12.24.png)

![Screenshot 2023-07-13 at 17.03.00](./AWS.assets/Screenshot 2023-07-13 at 17.03.00.png)



![Screenshot 2023-07-13 at 17.03.57](./AWS.assets/Screenshot 2023-07-13 at 17.03.57.png)

7

![Screenshot 2023-07-14 at 01.37.27](./AWS.assets/Screenshot 2023-07-14 at 01.37.27.png)

![Screenshot 2023-07-14 at 01.38.27](./AWS.assets/Screenshot 2023-07-14 at 01.38.27.png)

![Screenshot 2023-07-14 at 01.38.58](./AWS.assets/Screenshot 2023-07-14 at 01.38.58.png)



![Screenshot 2023-07-14 at 01.41.12](./AWS.assets/Screenshot 2023-07-14 at 01.41.12.png)

![Screenshot 2023-07-14 at 01.41.45](./AWS.assets/Screenshot 2023-07-14 at 01.41.45.png)



![Screenshot 2023-07-14 at 01.17.16](./AWS.assets/Screenshot 2023-07-14 at 01.17.16.png)

![Screenshot 2023-07-14 at 01.19.18](./AWS.assets/Screenshot 2023-07-14 at 01.19.18.png)

![Screenshot 2023-07-14 at 01.21.48](./AWS.assets/Screenshot 2023-07-14 at 01.21.48.png)

![Screenshot 2023-07-13 at 17.05.54](./AWS.assets/Screenshot 2023-07-13 at 17.05.54.png)

![Screenshot 2023-07-13 at 17.38.53](./AWS.assets/Screenshot 2023-07-13 at 17.38.53.png)

![Screenshot 2023-07-13 at 17.34.50](./AWS.assets/Screenshot 2023-07-13 at 17.34.50.png)

![Screenshot 2023-07-13 at 17.06.08](./AWS.assets/Screenshot 2023-07-13 at 17.06.08.png)

![Screenshot 2023-07-13 at 17.07.24](./AWS.assets/Screenshot 2023-07-13 at 17.07.24.png)

![Screenshot 2023-07-13 at 17.09.26](./AWS.assets/Screenshot 2023-07-13 at 17.09.26.png)





### Exercise 8.4

![Screenshot 2023-07-10 at 16.19.20](./AWS.assets/Screenshot 2023-07-10 at 16.19.20.png)

1

![Screenshot 2023-07-14 at 02.04.06](./AWS.assets/Screenshot 2023-07-14 at 02.04.06.png)

![Screenshot 2023-07-14 at 02.04.25](./AWS.assets/Screenshot 2023-07-14 at 02.04.25.png)



2

![Screenshot 2023-07-14 at 02.06.15](./AWS.assets/Screenshot 2023-07-14 at 02.06.15.png)

![Screenshot 2023-07-14 at 02.06.31](./AWS.assets/Screenshot 2023-07-14 at 02.06.31.png)



3

![Screenshot 2023-07-14 at 02.08.45](./AWS.assets/Screenshot 2023-07-14 at 02.08.45.png)



4

![Screenshot 2023-07-14 at 02.10.36](./AWS.assets/Screenshot 2023-07-14 at 02.10.36.png)



5

![Screenshot 2023-07-14 at 02.15.23](./AWS.assets/Screenshot 2023-07-14 at 02.15.23.png)



6

![Screenshot 2023-07-14 at 02.16.55](./AWS.assets/Screenshot 2023-07-14 at 02.16.55.png)





![Screenshot 2023-07-14 at 02.23.29](./AWS.assets/Screenshot 2023-07-14 at 02.23.29.png)



![Screenshot 2023-07-14 at 02.18.18](./AWS.assets/Screenshot 2023-07-14 at 02.18.18.png)



![Screenshot 2023-07-14 at 02.24.44](./AWS.assets/Screenshot 2023-07-14 at 02.24.44.png)

![Screenshot 2023-07-14 at 02.39.24](./AWS.assets/Screenshot 2023-07-14 at 02.39.24.png)

![Screenshot 2023-07-14 at 02.42.10](./AWS.assets/Screenshot 2023-07-14 at 02.42.10.png)

7

![Screenshot 2023-07-14 at 02.44.29](./AWS.assets/Screenshot 2023-07-14 at 02.44.29.png)

8

![Screenshot 2023-07-14 at 02.57.34](./AWS.assets/Screenshot 2023-07-14 at 02.57.34.png)

![Screenshot 2023-07-14 at 02.57.48](./AWS.assets/Screenshot 2023-07-14 at 02.57.48.png)

![Screenshot 2023-07-14 at 02.58.12](./AWS.assets/Screenshot 2023-07-14 at 02.58.12.png)

![Screenshot 2023-07-14 at 02.58.36](./AWS.assets/Screenshot 2023-07-14 at 02.58.36.png)

https://www.youtube.com/watch?v=zkfNyQQ-NFk
