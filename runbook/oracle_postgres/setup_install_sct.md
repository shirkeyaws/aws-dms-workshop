## Setup AWS Schema Conversion Tool

In this step, you will install the AWS Schema Conversion Tool locally.

> *For those participants not wishing to install the AWS Schema Conversion Tool locally, you can use the Schema Conversion Tool via Amazon AppStream 2.0 resources that will have been temporarily provisioned for your use during this lab. See [Setup: Accessing Amazon AppStream 2.0 Tools](#setup-accessing-amazon-appstream-tools)*

### AWS SCT Download

Download the latest version of AWS Schema Conversion Tool (SCT) from the following link:

> <http://amzn.to/aws-sct> (=> <http://docs.aws.amazon.com/SchemaConversionTool/latest/userguide/CHAP_SchemaConversionTool.Installing.html>)

> *If you already have SCT installed, we recommend that you download and install the latest version*

### Download JDBC Drivers

For connecting to your source database (Oracle) and target database (PostgreSQL), you will need the appropriate JDBC drivers for both databases. If you have not already done so, download the [JDBC Drivers](#setup-jdbc-drivers) before moving forward.

### Configure AWS SCT with JDBC Drivers

Once downloaded, launch AWS Schema Conversion Tool. On first launch, you will be presented with a terms and conditions statement, click **Agree** if you agree to the terms and conditions specified.


Next, you should see the following page:

![AWS Schema Conversion Tool: Initialized](images/setup/aws_sct/init.png)

Click on **Settings** > **Global Settings**

Now you should see the following Global Settings dialog:

![AWS Schema Conversion Tool: Global Settings](images/setup/aws_sct/globals.png)

Make the following changes to the Global Settings:

- Select **Drivers** on the left-side panel
- For the **Oracle Driver Path**, select the location of your local Oracle jar file
- For the **PostgreSQL Driver Path**, select the location of your local PostgresSQL jar file
- Click **OK** to Proceed

TODO: remove the following as permissions are completely open now

### Permit Local Access to Source/Target Databases

You will now modify both Source and Target database permissions so that you can connect to those databases with the AWS SCT locally. 

To do so, you will modify the Security Groups attached to the databases. The following link will provide you acces to the list of Security Groups in the region, filtered by the default CloudFormation stack name of **workshop**:

> <http://amzn.to/aws-tokyo-sg-workshop> (=> <https://ap-northeast-1.console.aws.amazon.com/ec2/v2/home?region=ap-northeast-1#SecurityGroups:search=workshop;sort=groupId>)

The list should look similar to the following, with two different SGs created by the earlier CloudFormation template, one for Oracle and the other for PostgreSQL:


![AWS Schema Conversion Tool: List of Security Groups](images/setup/aws_sct/sg-list.png)

Open the following ports to provide access from your current IP address.

- Modify **workshop-oracle-sg** Security Group as follows:
    - Add rule Oracle Port – 1521 > Open to ‘My IP’
- Modify **workshop-postgres-sg** Security Group as follows:
    - Add rule Postgres Port – 5432 > Open to ‘My IP’

[](TODO: describe/screenshot this step)