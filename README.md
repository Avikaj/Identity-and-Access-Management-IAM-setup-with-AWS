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
