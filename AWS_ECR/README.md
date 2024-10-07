# Sample ToDo App in React - Build for AWS ECR

## Build Docker Image
To build the Docker image for the ToDo app, use the following command:

```bash
docker build -t demotodo-app .
OR
docker build -t demotodo-app Dockerfile
```
## Push to AWS ECR

1. Authenticate Docker to AWS ECR
Retrieve an authentication token and authenticate your Docker client to your registry. Use the AWS CLI:
```
aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin 469264496762.dkr.ecr.ap-south-1.amazonaws.com
```
2. Tag the Docker Image
After the build completes, tag your image so you can push it to the AWS ECR repository:
```
docker tag demotodo-app:latest 469264496762.dkr.ecr.ap-south-1.amazonaws.com/demodocker-repo:latest
```
3. Push the Docker Image to AWS ECR
Finally, push the image to the ECR repository:
```
docker push 469264496762.dkr.ecr.ap-south-1.amazonaws.com/demodocker-repo:latest
```
