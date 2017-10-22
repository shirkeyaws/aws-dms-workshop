\newpage

## Objective

In this lab, you will be performing a migration from Oracle to PostgreSQL using SCT and DMS

### High Level Steps

- Lab Setup
    - Create EC2 Key Pair
    - Launch AWS CloudFormation Stack
    - Access Amazon AppStream 2.0 Tools
    - Install AWS Schema Conversion Tool (Optional)
    - Install Database Management Tool (Optional)
- Lab Steps
    - Create AWS Database Migration Instances
    - Connect to your environment
    - Setup AWS Schema Conversion Tool
    - Convert the Oracle schema to PostgreSQL
    - Create Source Endpoint in AWS DMS
    - Create Target Endpoint in AWS DMS
    - Create a Migration Task in AWS DMS
    - Start the migration
    - Generate transactions on Oracle and see the data being migrated to PostgreSQL - CDC
- Lab Teardown
    - Delete AWS CloudFormation Stack
    - Delete EC2 Key Pair