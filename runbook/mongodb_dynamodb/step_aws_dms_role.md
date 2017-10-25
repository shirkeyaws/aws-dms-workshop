

## Create AWS DMS Role

To access Amazon DynamoDB from AWS DMS, we need to create an IAM service role.

![AWS DMS Role - IAM Console](images/step/aws_dms_role/1.png)

![AWS DMS Role - Create IAM Role](images/step/aws_dms_role/2.png)

![AWS DMS Role - Select 'AWS Service'](images/step/aws_dms_role/3.png)

![AWS DMS Role - Select 'DMS'](images/step/aws_dms_role/4.png)

![AWS DMS Role - Attach Permissions](images/step/aws_dms_role/5.png)

![AWS DMS Role - Filter for DynamoDB Permissions](images/step/aws_dms_role/6.png)

![AWS DMS Role - Add Role Name](images/step/aws_dms_role/7.png)

Specify the role name **dms-workshop-dynamodb-role** and click **Create role**

![AWS DMS Role - Filter Roles to find new role](images/step/aws_dms_role/8.png)

![AWS DMS Role - View Details, Note the ARN for later](images/step/aws_dms_role/9.png)
