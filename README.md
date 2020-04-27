# Importing a VM as an Image using VM Import/Export on AWS

You can use VM Import/Export to import virtual machine (VM) images from your virtualization environment to Amazon EC2 as Amazon Machine Images (AMI), which you can use to launch instances.

Subsequently, you can export the VM images from an instance back to your virtualization environment.





# VM Import Export | Steps |

> Prerequisite: Download , install and configure AWS Command Line Interface

1. Export VM from its current environment as an OVA file (or VMDK, VHD, or RAW) if your are testing this make sure the VM has atleast one user configured with password)

2. Create a S3 bucket and upload the VM image to S3 using upload/drag and drop or using AWS CLI

3. Import your VM using the **ec2 import-image** command

4. Use the **ec2-describe-import-image-tasks** command to monitor the import progress

5. Once Import is completed Launch EC2 Instance from the AMI created, or Copy the AMI to other region.