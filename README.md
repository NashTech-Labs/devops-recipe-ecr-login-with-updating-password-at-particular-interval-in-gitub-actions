# devops-recipe-ecr-login-with-updating-password-at-particular-interval-in-gitub-actions
devops-recipe-ecr-login-with-updating-password-at-particular-interval-in-gitub-actions

In this i called the ecr_password_updator.py file from the main.yml.
Where main.yml file contains the github-pipeline for my python application.
You need to change the org and repository as per your requirement in the ecr_password_updater.py file.
Also you have to create your own github personal-access-token .

Steps to test:

1. Add your aws credentials in repo as a secrets i.e
       AWS_ACCESS_KEY_ID
       AWS_SECRET_ACCESS_KEY
       
2. Add ECR_PASSWORD as a secret in you repo
       
2. Configure aws credentials into your githib-workflow  just like main.yml 'Configure AWS credentials' step

3. Trigger your workkflow

You will be able to see the ECR_PASSWORD value got uodated and you executing workflow successfully by pulling and pushing images from ecr .