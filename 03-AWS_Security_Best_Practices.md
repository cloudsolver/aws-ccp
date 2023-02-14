# AWS Security Best Practices


## Root User
* Automatically created when you create an AWS account
* Protect with MFA (Multi-factor authentication)
* Only root user can delete the account
* There is just one root user

_Best Practice:_ Identity and Access Management - create a new user and provide a role. Never use the root user unless absolutely required.

VPC - Vitual Private Cloud. Default VPC will always be created for you.
* AWS Management Console
    * Easy to navigate via web-browser
    * Good for non-technical roles
Use the search feature for easy access.
* AWS CLI - same features as the management console
    * New features show up here first 
    * Programmatic access provides access to your AWS resources
* AWS SDK - can be leveraged to make changes to the environment via programmatic access. 

