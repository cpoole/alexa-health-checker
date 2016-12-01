Alexa Health Checker
===================

This is an Amazon Alexa skill that allows you to query the health status of your EC2 instances

----------------------------

###Configuring your AWS account

* Please create the following policy named `alexaHealthCheckerPolicy`

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Action": [
        "autoscaling:Describe*",
        "cloudtrail:DescribeTrails",
        "cloudtrail:GetTrailStatus",
        "cloudwatch:Describe*",
        "cloudwatch:Get*",
        "cloudwatch:List*",
        "ec2:Describe*",
        "ec2:Get*"
      ],
      "Effect": "Allow",
      "Resource": "*"
    }
  ]
}
```

* Please create the following role name `alexaHealthCheckerRole` and choose "Role for Cross-Account Access"
* Click the Select button for Allows IAM users from a 3rd party AWS account to access this account. For Account ID, enter 359853616165
* Assign the above policy to the role
* Click create role

###Configuring Alexa

Navigate to the configuration section inside the Alexa companion app and navigate to the Alexa Health Checker role.

Type in your account ID and the ARN of the role you just created


