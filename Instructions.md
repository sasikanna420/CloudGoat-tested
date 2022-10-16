
# Pre-Installed server

Follow below steps to access, 

•	Always switch to ap-south-1 region for the closer one. 

![image](https://user-images.githubusercontent.com/70305957/196031417-bf88d7b2-7d35-4723-bc5d-ee3c529cafe5.png)

•	Start & Stop the base server before and after testing phase.    

![image](https://user-images.githubusercontent.com/70305957/196030957-73cdb097-c1af-4a86-b031-ee9f5bf754a5.png)

•	Already server is installed with required packages. 

![image](https://user-images.githubusercontent.com/70305957/196031022-4ddc9c30-beb0-44fb-bab7-c3916c780ca7.png)

• Default profile set-up configured too, only left over is to execute below command always after instance started. 

```  
$ ./cloudgoat.py config whitelist --auto   
```
# Reason to execute always: It collects IP address and store it to whitelist for CIDR blocks. EC2 IP's are shuffled on every stop/start. 

# DO NOT CREATE ANY RESOURCE MANUALLY 

### Creating the Resource ###### 
```
$ ./cloudgoat.py create cloud_breach_s3  
```
```
$ ./cloudgoat.py create iam_privesc_by_attachment  
```
### Destroying the Resource ##### 
```
$ ./cloudgoat.py destroy cloud_breach_s3  
```
```
$ ./cloudgoat.py destroy iam_privesc_by_attachment
```






