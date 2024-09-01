# Identity-and-Access-Management-IAM-setup-with-AWS



## Step 1 : Create EC2 Instances with tags
Start by creating two EC2 instances on the AWS account.
Both of these instances should look like this with one tag called "Env" and value of "production" and "development" respectively.
<img width="1510" alt="production tag" src="https://github.com/user-attachments/assets/74f1cc21-dcea-4951-ad44-938bc9104296">
<img width="1512" alt="Development tag page" src="https://github.com/user-attachments/assets/b3a65041-38e5-45ad-ab00-2f2f5d3b1ac4">

## Step 2 : Create an IAM Policy
Navigate to the IAM console, go to Policies and start Create Policy
Here, paste the JSON file provided in this repository, which should look this this.
<img width="1512" alt="Screenshot 2024-09-01 at 2 15 58 PM" src="https://github.com/user-attachments/assets/f8bacb5e-eaa7-4ed7-a8f6-b0b15e8b1fca">
Go ahead and give a name to the policy and finish creating a new IAM policy.

## Step 3: Create an Account Alias
### An Account Alias is a friendly name for your AWS account that you can use instead of your account ID (which is usually a bunch of digits) to sign in to the AWS Management Console. This will be used by other users to access your account through this unique log-in URL.
#### In the right-hand side of the dashboard, choose "Create" under Account Alias.
<img width="477" alt="Screenshot 2024-09-01 at 2 35 23 PM" src="https://github.com/user-attachments/assets/2241fd61-3e80-4162-a5bd-9b29de67b03c">
