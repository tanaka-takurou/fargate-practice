# fargate practice
Practice projects for fargate.


## Requirements
- aws-cli
- docker environment


## Usage
### Build
```bash
docker build .
```

### Check
```bash
docker run sample-docker-image-id
```

### Push
```bash
aws ecr create-repository --repository-name sample-repository --region region
docker tag sample-docker-image-id aws_account_id.dkr.ecr.region.amazonaws.com/sample-repository
docker login -u AWS -p $(aws ecr get-login-password --region REGION) aws_account_id.dkr.ecr.REGION.amazonaws.com
docker push aws_account_id.dkr.ecr.region.amazonaws.com/sample-repository
```

### Clean Up
```bash
aws ecr delete-repository --repository-name sample-repository --region region --force
```
