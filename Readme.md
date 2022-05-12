# CREATING EC2 USING AWS CLI

## DEPENDENCIES

Install `AWSCLI`
In the python environment, we  can install awscli with the following command `Pip3 install awscli`
**Awscli configurations**
Aws configure is the fastest way to set up `awscli`. When we run this comand, awscli prompts with four pieces of information that is stored in the profile. The following are the information which we refer to credentials.
-Access key ID
-Secret access key
-Aws region
-Output format
After we are set with configuration we can create **vpc** and **subnet** for our ec2 instances. To create the vpc we use the following command and we also need to specify the cidr block.
`aws ec2 create-vpc --cidr-block 10.0.0.0/16`. You can specify your own `cidr block`.
To create a `subnet` we run the following command `aws ec2 create-subnet --vpc-id vpc-009b5a01df822f334 --cidr-block 10.0.0.0/16`. Here we and **vpc id** so that our **subnet** can be inside our **vpc**.
we need to create the `security group ids` as well as the `key pair`.
To create the `security group ids` we run the following comand `aws ec2 create-security-group --group-name MySecurityGroup --description "My security group" --vpc-id vpc-1a2b3c4d` here we specify the **vpc**.
To create `key pair` we run the following comand.`aws ec2 create-key-pair --key-name MyKeyPair --query 'KeyMaterial' --output text > MyKeyPair.pem` you can name your key anything and by default `.pem` is the default output if we do not specify our prefered output.
After we done 

### using python boto3
you setup python vertual enviroment after that, you can do the following commands.

-pip install **boto3**
-pip install **awscli** so that you can you use it to do your aws configure  as it is not advisable to enter your configuration in the code.

