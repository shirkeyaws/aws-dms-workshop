## Create an AWS SCT Project

In AWS SCT, select **File** > **New Project Wizard**

![AWS SCT New Project Wizard](images/step/aws_sct_new_project/init.png)

### New Project Wizard – Select Source

Enter the following in the dialog displayed:

![AWS SCT New Project Wizard - Step 1](images/step/aws_sct_new_project/dialog-step-1.png)

- **Project Name** | DMS-Workshop-Oracle2PostgreSQL|
- **Location**: (leave default)
- For **Source Database Engine**, specify:
    - Transactional Database (OLTP) 
    - Oracle
    - I want to switch engine and optimize for the cloud

Click **Next** to continue

### New Project Wizard – Connect to Source Database

Enter the following in the next dialog displayed:


- **Type**:	SID
- **Server Name**: (enter DNS name of your Oracle instance)
- **Server Port**: 1521
- **Oracle SID**: (enter database name, default is Oracle)
- **User name**: dbmaster
- **Password**: (enter the password for your Oracle instance)
- **Oracle Driver Path**: (see notes below)
    - Local: when running AWS SCT locally, then the JDBC jar file for Oracle must be selected from where it was downloaded to earlier
    - DMS Workshop AppStream 2.0 Clients: the path is **C:\\Drivers** as shown below: 
    - ![AWS SCT New Project Wizard - Driver Location on AppStream](images/step/aws_sct_new_project/appstream-jdbc-dir.png)

When finished, click **Test Connection**. If you receive a **Connection Successful** message, then proceed, otherwise reconfirm the values you have entered earlier and try again.

![AWS SCT New Project Wizard - Test Source Connection](images/step/aws_sct_new_project/test_connection_success.png)

### New Project Wizard - Select Schema

From the Select Schema step, select **DBMASTER** as the Source Schema

![AWS SCT New Project Wizard - Select Schema](images/step/aws_sct_new_project/select-schema.png)

### New Project Wizard - Run Database Migration Assessment

![AWS SCT New Project Wizard - Database Migration Assessment](images/step/aws_sct_new_project/run-dma.png)

### New Project Wizard - Select Target

![AWS SCT New Project Wizard - Select Target](images/step/aws_sct_new_project/select-target.png)

### New Project Wizard - Test Target Connection

![AWS SCT New Project Wizard - Test Target Connection](images/step/aws_sct_new_project/test-target-success.png)
