building docker image and pushing to ECR.

3 steps :

   -> aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin         319255955334.dkr.ecr.us-east-1.amazonaws.com

   -> docker build -t 319255955334.dkr.ecr.us-east-1.amazonaws.com/roboshop/catalogue:latest .

   -> docker push 319255955334.dkr.ecr.us-east-1.amazonaws.com/roboshop/catalogue:latest 

 * In jenkins u need to download AWS plugin ---->AWS STEPS (for aws credentials)
 * which will help to access credentials of amazon to enter into it access ECR to store docker image after buiding and tagging with respective name. 