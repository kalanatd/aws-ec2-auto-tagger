# aws-ec2-auto-tagger
Automatically Tagging EC2 Instances upon creation and sending a Slack Alert using  Cloudtrail logs.

When an EC2 is created AWS Cloudwatch events rule will be triggered and and that rule will invoke a lambda function.
Within that lambda function the cloudtrail event data generated by the EC2 creation event is parsed and add the IAM user data + other relevant data as Tags.

![image](https://user-images.githubusercontent.com/39367522/167817086-da7e7411-ce8e-41e4-bcc2-646bb0347a68.png)

Once the "Owner" tag is added, check for other pre-defined mandatory tags. If atleast one of them is missing a Slack alert will be sent with the missing tags, expected Tag Values. 


 
Find the complete Guide on here. [Automatically tag AWS EC2 Instances with the “Owner” tag upon creation](https://grumpysysadmin.medium.com/automatically-tag-aws-ec2-instances-with-the-owner-tag-upon-creation-7ea7b230a2d0).

Inspired by and initial code base from https://aws.amazon.com/blogs/mt/auto-tag-aws-resources/

https://github.com/aws-samples/resource-auto-tagger


