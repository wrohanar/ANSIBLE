# GitLab CI/CD for Terraform | Plan, Apply, Destroy: Managing Infrastructure

Table of contents <br>
Step1: create an IAM user <br>
Step2: Create Gitlab Account<br>
Step3: Terraform Files<br>
Step4: Variables setup in Gitlab (Secrets)<br>
Step5: GitLab CI/CD configuration<br>
Step6: .gitlab-ci.yml<br>
Step7: Destroy<br>

# Step1: create an IAM user
1. Navigate to the AWS console. <br>
2. Search for IAM and click "Users." <br>
3. Add a new user, specifying a name like "Terraform." <br>
4. Attach the "AdministratorAccess" policy. <br>
5. Create an access key and download the CSV file. <br>


# Step2: Create Gitlab Account<br>
1. Visit GitLab. <br>
2. Register for an account or use the GitHub login option. <br>
# Step3: Terraform Files<br>

Create a blank repository on GitLab and add the following Terraform files:<br>

main.tf: Defines AWS resources.<br>
provider.tf: Configures the AWS provider.<br>
install_jenkins.sh: Shell script for Jenkins installation.<br>
backend.tf: Configures Terraform backend.<br>

# Step4: Variables setup in Gitlab (Secrets)<br>
Inside your GitLab repository:<br>

Go to Settings -> CI/CD.<br>
Expand the variables section.<br>
Add the following variables with corresponding values:<br>
AWS_ACCESS_KEY_ID<br>
AWS_SECRET_ACCESS_KEY<br>
# Step5: GitLab CI/CD configuration<br>
Create a .gitlab-ci.yml file in your repository with the specified stages and jobs. Refer to the provided example.<br>
# Step6: .gitlab-ci.yml<br>
Refer to the full .gitlab-ci.yml configuration provided in the repository.<br>


# Step7: Destroy<br>
Manually trigger the "destroy" stage in GitLab CI/CD to delete resources.<br>


### Special thanks to Ajay Kumar Yegireddi


