# CloudGoat-tested

CloudGoat is Rhino Security Labs' "Vulnerable by Design" AWS deployment tool. It allows you to hone your cloud cybersecurity skills by creating and completing several "capture-the-flag" style scenarios. Each scenario is composed of AWS resources arranged together to create a structured learning experience.

Hereby we have tested the codes from cloudgoat and merged with some changes. 

# PRE_REQUISITE 

•	Linux or MacOS. Windows is not officially supported.

# Local Setup     

•	Python3.6+ is required.     
  https://docs.python-guide.org/starting/install3/linux/    
  
•	Terraform >= 0.14 installed and in your $PATH.     
  https://www.fosstechnix.com/how-to-install-terraform-on-linux/   

•	The AWS CLI installed and in your $PATH, and an AWS account with sufficient privileges to create and destroy resources.     
  https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html   
  
  ![image](https://user-images.githubusercontent.com/70305957/194966049-e4d7ea87-0715-425c-aa8a-c8b5c6cb781e.png)   

•	jq  
  https://stedolan.github.io/jq/

# One Time Setup 
```
git clone https://github.com/sasikanna420/CloudGoat-tested.git 
cd CloudGoat-tested
pip3 install -r ./requirements.txt 
chmod +x cloudgoat.py 
```
You may also want to run some quick configuration commands - it'll save you some time later:
```
$ ./cloudgoat.py config profile       
$ ./cloudgoat.py config whitelist --auto   
```
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

