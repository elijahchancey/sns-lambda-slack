# sns-lambda-slack
This project creates a lambda function which ingests SNS Notifications and sends them to a Slack Channel.  

A Cloudformation template creates the Lambda Function, SNS Topic and dependencies.  

To use it:
1) Create an Incoming Webhook Integration with Slack. It will produce a webhook URL, which you should then insert into the webhook_url variable in the Cloudformation template.
2) Create the Cloudformation stack using the template. 
3) The Cloudformation stack will create an SNS Topic you can use. Configure your Elastic Beanstalk Environments, RDS, etc, to send Notifications to this SNS Topic. The Topic ARN can be found in the Outputs section of the Cloudformation stack.
