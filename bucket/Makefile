BUCKET=aws-dms-workshop
REGION=ap-northeast-1
PROFILE=default

.Phony: all 

# please contact shirkeys@ if you need access keys for this project bucket
all: 
	aws s3 sync --delete --exclude Makefile --profile $(PROFILE) --region $(REGION) . s3://$(BUCKET)