# Overview of AWS 2.0 setup

Currently, all Amazon Web Services applications (except Solr) run under one account with the login `joey@artsy.net`, and each software engineer has an IAM user for that account.

**Only IAM users** should be used to log in.

We maintain 3 separate AWS accounts to better separate development, staging, and production environments. IAM users in the `ArtsyEngineering` group have access to the Dev environment, which can be reached by clicking on the dropdown with your name and choosing `Switch Role`. You can switch back to your main IAM account by choosing "back to [your name]" in the dropdown.

Engineers in the `ArtsyStaging` and `ArtsyProduction` groups will have access to those accounts.

The process that was used to set up cross-account access is described [here](https://blogs.aws.amazon.com/security/post/Tx70F69I9G8TYG/How-to-Enable-Cross-Account-Access-to-the-AWS-Management-Console), but only Tasks 1 and 2 are needed now.

At the moment, there are no systems running in these stacks, but the plan is to move all systems to one or more of these three over time. All new projects should use the new accounts.

The links an IAM user can use for one-time setup of their Role switching are below. When you click on the link, we recommend entering _development_, _staging_, and _production_ for the descriptions and green, yellow, and red (respectively) for the colors.

* [development](https://signin.aws.amazon.com/switchrole?account=857168411456&roleName=CrossAccountSignin)
* [staging](https://signin.aws.amazon.com/switchrole?account=468683317992&roleName=CrossAccountSignin)
* [production](https://signin.aws.amazon.com/switchrole?account=404343144811&roleName=CrossAccountSignin)

[MFA authentication](http://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_enable.html) must be enabled on your account to gain access to Production.

### To set up new users:

* Create a new IAM user in the main Artsy account and give them their username, password, and AWS ID and Secret.
* Add them to the `ArtsyEngineering` group to give them access to the dev environment.
* Ask them to login [here](https://artsy.signin.aws.amazon.com/console) and then click on [this link](https://signin.aws.amazon.com/switchrole?account=857168411456&roleName=CrossAccountSignin) to set up their access to the dev environment. They should put in "Development" for the description on that page.

### To assume a role in the AWS CLI

Follow the AWS instructions on [cross account roles](http://docs.aws.amazon.com/cli/latest/userguide/cli-roles.html#cli-roles-xaccount).

Your `~/.aws/credentials` file should resemble [this](https://gist.github.com/bhoggard/3635483f623aa0116451).