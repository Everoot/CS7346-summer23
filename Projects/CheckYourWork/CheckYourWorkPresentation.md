## 开场

Good evening everyone, we are group 6. At the end of this 10 minutes, you will know things about checkyourwork you don't know now. Let's get started. ▶️



## 介绍课题

So why need check your work?  ▶️

For now a university has greatly expanded its CS course and wants to be able to automate the grading of simple programming assignments. Students are able to upload their source code, which will be run and graded. Grades and runs must be persistent and auditable. 

For requirement,  ▶️ our group set up learning management system which can allow students, teachers, administrator access. This is login interface. ▶️ After login you can see something like this. Its has some functions look like canvas.  ▶️ This auto grading interface, our system can automatically grade student code assignment ▶️, and detect plagiarism with turnitin plugin. And all things are use AWS. ▶️ 

**(1 min)**





## 架构

Here is our project cloud architecture.

The First is Amazon Route 53, We set up our domain name “checkyourworkgroup.online” on godaddy. Users can visit the our website as “www.checkyourworkgroup.online"

Second is Amazon CloudFront, providing low latency access our website.

Third is AWS Certificate Manager, which manages secure sockets layer certificates for secure, protect public and private resources.

Fourth is Application Load Balancer: automatically distributes incoming traffic to our project web servers. 

Fifth is Network Address Translation (NAT) gateway allows outbound traffic for resources, user can access the resource use public ip address.

The Sixth is Auto Scaling group: Our system is deployed instances across multiple Availability Zones (AZs), which are deployed in a separate private subnet for additional security. 

The Seventh is EC2, where we deploy our system and set up the website. We use the local database mysql in the instance. Save upload files on EC2.

The Eighth is AWS offer some tools to help us to develop and deploy our system to EC2. 

The last two parts are plugins, the ninth is called turnitin which can detect plagiarism. The last one is Virtual programming Lab it can grade the student code automatically. (3 min)

**(3-4 min)**

▶️ 



## 优缺点(2 min)

For our project, in terms of priorities, we believe that Security, Performance, Availability, and Usability need to be prioritized. For security, because our system will has some private information about students and teachers, if leak information it will lead to a series of social problem. 

About performance, inadequate resource provisioning can lead to slow response times and poor user experience might lead to Performance Risk.

Then there is Availability, as the basis of the school's project, students and teachers should be available everyday during the use process to adapt to various learning plans. 

Finally, Usability, our project is a user-friendly interface that enables students and teachers to easily navigate and effectively use the platform. 

 ▶️  



### Advantages

Now let's talk about advantages

For Cost effective, In the course of the project, we found that AWS services like EC2 allow us to scale our resources based on our needs. I only pay for the services I use. This can be more cost-effective than maintaining your own physical servers.

For security, AWS also provides several features to ensure the security of my application, such as access control, Security Groups for firewall settings, and data encryption for stored data.

For low latency, with AWS's global infrastructure, we can deliver our project LMS to users around the world with low latency.▶️ 



### Limitations

AWS offers a wide range of services, and navigating these options can be complex. It requires understanding the interactions between services and the best ways to configure them to meet users needs. And while AWS can be cost-effective, it's also easy to incur additional costs if services are not properly monitored and managed. 



Of course it also has some risks, like downtime risk, performance risk, privacy risks, lock-in risk. Even Aws has already offer some mitigation techniques like snapshot features of Relational database service. Amazon CloudWatch, and so on. This may require significant time investment or sometimes need to hire AWS experts to solve the problem.▶️ 



## Demo

Now it is demo time. ▶️ 

This is our project domain name. For now I log in as administrator. This is our system interface. I can create courses, publish homework.

Now I swift to edit mode. I can use turnitin plugin to publish assignment here or other kinds of activities to course. 

For here I already create programming homework. I put some test case here. There already has two submission. We can check. For this jojo one. We can run online. And it will automatically grade. We can change code a little. And run it. You can see it has been graded automatically and return some feedback. The system very powerful, it can be easily modified by different requirements.

**( 1 min 30s)**

▶️ 





Now come back. About contributions,

In my opinion, our cloud platform project indeed has high commercial and academic value in the future. For the school, this project can greatly save the arrangement and correction of programming assignments. For students, this service can know their mistakes more quickly, so as to correct them in time. Our group proposed and implemented a feasible cloud architecture. We can offer an example for other developers.

**(<30s)**



▶️ 

Our group salute for everyone here.































































