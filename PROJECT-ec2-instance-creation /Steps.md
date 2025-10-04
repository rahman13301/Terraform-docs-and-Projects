# Overview of steps
Create a directory for your Terraform project and create a Terraform configuration file (usually named main.tf) in that directory. In this file, you define the AWS provider and resources you want to create. Here's a basic example:
```
   provider "aws" {
     region = "us-east-1"  # Set your desired AWS region
   }

   resource "aws_instance" "example" {
     ami           = "ami-0c55b159cbfafe1f0"  # Specify an appropriate AMI ID
     instance_type = "t2.micro"
   }
```
## Initialize Terraform:
In your terminal, navigate to the directory containing your Terraform configuration files and run:
```
terraform init
```
<img width="1045" height="345" alt="image" src="https://github.com/user-attachments/assets/72f31f4b-180f-4533-b6af-f45c184bf2c9" />

This command initializes the Terraform working directory, downloading any necessary provider plugins

## Plan the Configuration:
Before applting you can plan the configurations:
```
terraform plan
```
<img width="1287" height="666" alt="image" src="https://github.com/user-attachments/assets/14766226-2eed-4ddd-9875-5f6026709189" />


## Apply the Configuration:

Run the following command to create the AWS resources defined in your Terraform configuration:
```
terraform apply
```
<img width="1281" height="661" alt="image" src="https://github.com/user-attachments/assets/ece645dc-4372-4a01-b014-64a9b1484eff" />

- Now you can see instance is created in codespace as well as in AWS console.
  <img width="849" height="273" alt="image" src="https://github.com/user-attachments/assets/9999d245-828f-44ff-89ad-bcc1512cb083" />
  <img width="1632" height="206" alt="image" src="https://github.com/user-attachments/assets/bb91ebd4-54d0-4e1d-8406-b0f6844234eb" />
  <img width="1446" height="595" alt="image" src="https://github.com/user-attachments/assets/50e47d1e-d727-4e18-9321-75c2e443934a" />


Terraform will display a plan of the changes it's going to make. Review the plan and type "yes" when prompted to apply it.

You can see terraform state file is created.
<img width="1179" height="205" alt="image" src="https://github.com/user-attachments/assets/b0cdc370-b35b-48d1-962d-bd6568689da2" />


## Verify Resources:
After Terraform completes the provisioning process, you can verify the resources created in the AWS Management Console or by using AWS CLI commands.

## Destroy Resources:
If you want to remove the resources created by Terraform, you can use the following command:
```
terraform destroy
```
<img width="1284" height="528" alt="image" src="https://github.com/user-attachments/assets/77503b0a-8c98-4ab3-8211-58990c016bfa" />
<img width="934" height="368" alt="image" src="https://github.com/user-attachments/assets/a552eff7-b68d-4cb5-b196-b68b197cbe18" />
<img width="1397" height="176" alt="image" src="https://github.com/user-attachments/assets/fba42aea-03bb-4ec8-b610-098976a21f78" />


Be cautious when using terraform destroy as it will delete resources as specified in your Terraform configuration.
