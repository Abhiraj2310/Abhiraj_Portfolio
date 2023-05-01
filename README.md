# demo-actions-project

#Prerequisites:
Before we start, we should have the following prerequisites:

1. An AWS account
2. A Github Account
3. A static website with HTML, CSS, and JavaScript files

#Project Steps:

#Create an S3 bucket:

1. Log in to the AWS Management Console and go to the S3 service
2. Click "Create Bucket" and follow the prompts to create a bucket with a DNS name

#Configure bucket properties:

1. Enable static website hosting in the bucket properties
2. Specify an index document and error document for your website
3. Enable public access

#Configure Github Actions and IAM

1. Create an IAM user in the AWS console with the necessary permissions to perform the actions you want to automate in your GitHub Actions workflow. Be sure to save the Access Key ID and Secret Access Key for the IAM user.

2. In your GitHub repository, create a new directory named `.github/workflows`.

3. In the `.github/workflows` directory, create a new YAML file with a name that reflects the purpose of your workflow (e.g., `main.yml`).

4. In the YAML file, define your workflow using the GitHub Actions syntax. This will typically involve specifying a trigger, defining one or more jobs, and specifying the steps to be executed in each job.

5. In one of the steps in your workflow, add a command to set the AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY environment variables to the values of the IAM user's Access Key ID and Secret Access Key.

Once you have completed these steps, your GitHub Actions workflow will be triggered when the specified trigger event occurs (e.g., a push to the master branch), and the workflow will use the IAM user's Access Key ID and Secret Access Key to perform the necessary actions in your AWS environment.

#Adding static website Index.html to host

Commit your index.html page to the repository this will trigger the Github Actions and your Index.html file will be sent to the S3 Bucket.

#Verify the website is working:

Verify the website is working by using bucket website endpoint.

