# Identity-and-Access-Management-IAM-setup-with-AWS
## What is AWS IAM?
AWS Identity and Access Management (IAM) is used to control who is authenticated (signed in) and authorized (has permissions) to use your account's resources. 

## Project Layout
### The layout of the project looks like this:
<img width="797" alt="Screenshot 2024-09-01 at 7 08 16 PM" src="https://github.com/user-attachments/assets/9a637a06-5d3b-4ae9-8792-acfa9b61dbce">



## Step 1 : Create EC2 Instances with tags
### Amazon EC2 is a service that lets you rent and use virtual computers in the cloud. They're like your personal computers, but they exist on the internet instead of being physically in front of you. You can create, customize, and use these computers for all different reasons, from running applications to hosting websites.
Start by creating two EC2 instances on the AWS account.
Both of these instances should look like this with one tag called "Env" and value of "production" and "development" respectively.
<img width="1510" alt="production tag" src="https://github.com/user-attachments/assets/74f1cc21-dcea-4951-ad44-938bc9104296">
<img width="1512" alt="Development tag page" src="https://github.com/user-attachments/assets/b3a65041-38e5-45ad-ab00-2f2f5d3b1ac4">

## Step 2 : Create an IAM Policy
### An IAM policy is a rule for who can do what with your AWS resources. It's all about giving permissions to IAM users, groups, or roles, saying what they can or can't do on certain resources, and when those rules kick in.
Navigate to the IAM console, go to Policies and start Create Policy
Here, paste the JSON file provided in this repository, which should look this this.
<img width="1512" alt="Screenshot 2024-09-01 at 2 15 58 PM" src="https://github.com/user-attachments/assets/f8bacb5e-eaa7-4ed7-a8f6-b0b15e8b1fca">
Go ahead and give a name to the policy and finish creating a new IAM policy.

## Step 3 : Create an Account Alias
### An Account Alias is a friendly name for your AWS account that you can use instead of your account ID (which is usually a bunch of digits) to sign in to the AWS Management Console. This will be used by other users to access your account through this unique log-in URL.
In the right-hand side of the dashboard, choose "Create" under Account Alias.
<img width="477" alt="Screenshot 2024-09-01 at 2 35 23 PM" src="https://github.com/user-attachments/assets/2241fd61-3e80-4162-a5bd-9b29de67b03c">

## Step 4 : Create IAM User Groups 
### IAM user groups are the collections/folders of users. It allows you to manage permissions for all the users in your group at the same time by attaching policies to the group rather than individual users.
Navigate to "Create user group" from the left-hand navigation panel under "User groups".
Enter your User Group name and attach the policy created earlier to inherit all the permissions.
<img width="1511" alt="User group" src="https://github.com/user-attachments/assets/6741c258-565c-494c-bd47-1b94c5d24dcb">

## Step 5 : Create IAM users
### IAM users are the people that will get access to your resources/AWS account.
Navigate to "Create user" from the left-hand navigation panel under "Users".
Enter the user name and tick the checkbox for Provide user access to the AWS Management Console to provide console access to the user to use AWS services.
Uncheck the box for Users must create a new password at next sign-in - Recommended.
<img width="1510" alt="Screenshot 2024-09-01 at 3 03 56 PM" src="https://github.com/user-attachments/assets/d9a42253-66a8-4f9f-8c69-2c6e34b62d0a">

## Step 6 : Add the newly created user to the User Group
Right after clicking on "next" after Step 4, choose the existing User Group from the list.
<img width="1506" alt="Screenshot 2024-09-01 at 3 06 40 PM" src="https://github.com/user-attachments/assets/19c27b91-bfed-4e84-9425-45dfe2096cba">

After this hit "next" again and then "Create User".

## Step 7 : Testing User Access
### This step is to see if permissions are successfully given and the user can access the console and services smoothly or not.
Copy the console sign-in URL from the page you are on. Open a new Incognito tab on the browser and paste the URL.
Using the User name and Console password given in your IAM tab, log in.
<img width="1512" alt="Screenshot 2024-09-01 at 3 15 23 PM" src="https://github.com/user-attachments/assets/683d7762-9ee8-4558-a437-6cf8b527e8fd">

### When you are successfully logged in to your user account, you will see that you are not able to access a lot of stuff. That is because the user is not given all the permissions to do so, such as deleting one of the instances that were created initially.
And that is exactly what I inteded to do in this project!


