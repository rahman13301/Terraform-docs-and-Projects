## Codespace in GitHub:

 It looks like VS code built in feature inside GuitHub repository. It can be accessible for 60 hours free in a month, which include 2 CPUs and 4 GB RAM contained.

**Goto Github repository > Click on Code & Codesapce > Create code sapce** :

<img width="571" height="336" alt="image" src="https://github.com/user-attachments/assets/b838291c-55cb-4aed-878f-1ca8e6576a76" />


<img width="761" height="94" alt="image" src="https://github.com/user-attachments/assets/6672284f-022b-4d70-a775-a4e24a0d7b4e" />
<img width="748" height="109" alt="image" src="https://github.com/user-attachments/assets/829b7512-0df8-44d3-913b-a0d5c2afc99d" />
<img width="761" height="229" alt="image" src="https://github.com/user-attachments/assets/56cf8dd8-6cf1-4e32-80bc-e177b62ca785" />
<img width="758" height="172" alt="image" src="https://github.com/user-attachments/assets/1024a4b7-01cc-410d-af83-4938ecc05625" />

**Search for rebuild and do rebuild, it will take around 5 minutes to build**

<img width="822" height="103" alt="image" src="https://github.com/user-attachments/assets/e7cde2dc-c6ff-4d9d-9a46-3ce9dc7624ce" />

**Once done check the Terraform and AWS configurations as below:**

<img width="602" height="85" alt="image" src="https://github.com/user-attachments/assets/53998413-54ad-4101-8c28-69e71f2cf64d" />
<img width="1231" height="593" alt="image" src="https://github.com/user-attachments/assets/fed4421a-8363-4c44-aa00-9b5332e7c774" />



## Setup Terraform for AWS:

- Create an AWS IAM User:

 To configure AWS credentials and set up Terraform to work with AWS, you'll need to follow these steps:

 Install AWS CLI (Command Line Interface):

 Make sure you have the AWS CLI installed on your machine. You can download and install it from the [AWS CLI download page](https://aws.amazon.com/cli/).

- Create an AWS IAM User:

To interact with AWS programmatically, you should create an IAM (Identity and Access Management) user with appropriate permissions. Here's how to create one:

a. Log in to the AWS Management Console with an account that has administrative privileges.

b. Navigate to the IAM service.

c. Click on "Users" in the left navigation pane and then click "Add user."

Choose a username, select "Programmatic access" as the access type, and click "Next: Permissions."

Attach policies to this user based on your requirements. At a minimum, you should attach the "AmazonEC2FullAccess" policy for basic EC2 operations. If you need access to other AWS services, attach the relevant policies accordingly.

Review the user's configuration and create the user. Be sure to save the Access Key ID and Secret Access Key that are displayed after user creation; you'll need these for Terraform.

Configure AWS CLI Credentials:
Use the AWS CLI to configure your credentials. Open a terminal and run:
```
aws configure
```

<img width="852" height="330" alt="image" src="https://github.com/user-attachments/assets/4ef6ca36-e748-491d-a5a4-73995703ee41" />

- Codesapce is communicating with AWS
<img width="862" height="50" alt="image" src="https://github.com/user-attachments/assets/19af74b5-aca4-4685-a61b-171c23c0584f" />


It will prompt you to enter your AWS Access Key ID, Secret Access Key, default region, and default output format. Enter the credentials you obtained in the previous step.








