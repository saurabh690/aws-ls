# aws-ls
A project utilising different features of Amazon Web Services platform to create a full stack app. 

We have used instances of Ubuntu 18.04 and CentOS 7 for deploying our services on the cloud. 

**Tomcat** is deployed using the Ubuntu 18.04 AMI. The version used is 9.
**MySQL, RabbitMQ, Memcache** are deployed using the CentOS 7 AMI.

The application is prepared using maven from the local computer after which we add it our S3 Bucket to store on the cloud and get it on the Tomcat Instance after creating an IAM Role for the same. 

We used **Elastic Load Balancer** from AWS EC2 to balance the load on the AWS server. This has been used as a repacement for Nginx.

Finally, we use the ELB endpoint to connect to our domain to display the app on port 8080 from tomcat instance. Also we made the tomcat instance autoscaling to automatically manage it as per the requests.