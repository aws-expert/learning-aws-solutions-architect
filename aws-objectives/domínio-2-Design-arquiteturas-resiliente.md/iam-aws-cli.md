# IAM & AWS CLI
## IAM:  users and groups

- IAM = identity and acess management, global service.
- root account created by default shouldn't be used os shared.
- ssers are people inside the organization, and can be grouped.
- groups onlye contain users, not other groups.
- users don't have to belong to a group, and user can belong to multiple groups.

![aws-image](https://github.com/aws-expert/learning-aws-solutions-architect/blob/main/images/aws1.png)

## IAM Permissions
- users and groups can be assigned JSON documents called policies.
- these policies define the permissions of users.
- in aws you apply the least privilege principle: don't give more permissions than a user needs.

## IAM - Password Policy
- strong passwords = high security for your accounts
- in AWS you can set a password policy


## Multi Factor Authenticator
- users have access to your account and can possibly change configurations or delete resources in your AWS.


### MFA devices options in AWS
- virtual MFA device (Google Authenticator, Authy)
- universal 2nd factor (U2F) security key.
- hardware key fob MFA device
- hardware key fob MFA device for AWS govCloud (US).

## How users can access AWS?
- to access the AWS you have 3 options:
  - AWS management console
  - AWS command line interface (AWS CLI)
  - AWS software development kit (SDK)
- access key are generated throught the AWS console.
- users manage their own access keys.
- access keys are secret, just like a password. don't share them.
- access key ID = username
- secret access key = passwords.
- 









