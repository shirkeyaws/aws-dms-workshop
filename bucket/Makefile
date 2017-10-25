SOURCE:=*.yaml
BUCKET=aws-dms-workshop
REGION=ap-northeast-1
PROFILE=default

.Phony: validate all 

validate: $(SOURCE)
	- aws cloudformation validate-template --template-body file://workshop-lab-1.yaml
	- aws cloudformation validate-template --template-body file://workshop-lab-nosql-mongodb-dynamodb.yaml


# please contact shirkeys@ if you need access keys for this project bucket
all: validate
	aws s3 sync --delete --exclude Makefile --profile $(PROFILE) --region $(REGION) . s3://$(BUCKET)