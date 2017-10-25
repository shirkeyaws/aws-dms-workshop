### AWS DMS Tasks

The following link will display all **DMS Tasks** in this region

> <http://amzn.to/aws-tokyo-dms-tasks>
(=> <https://ap-northeast-1.console.aws.amazon.com/dms/home?region=ap-northeast-1#tasks:>)

#### AWS DMS Tasks -- List All

You should now see the following:

![AWS DMS Tasks - List Tasks](images/step/aws_dms_tasks/list-tasks.png)

#### AWS DMS Tasks - Create New

You will now create a new AWS DMS Task by clicking the **Create Task** button, which will display the following page:

![AWS DMS Tasks - Create Task (Detail)](images/step/aws_dms_tasks/create-task-1.png)

Within this page, you will enter the following data:

- **Task name**: dms-workshop-task-mongodb2dynamodb
- **Replication instance**: (defaults to **DMS Replication Instance** you created earlier)
- **Source endpoint**: (defaults to **DMS Endpoint** for the MongoDB source database that you created earlier)
- **Target endpoint**: (defaults to **DMS Endpoint** for the DynamoDB target database that you created earlier)
- **Migration type**: Migrate existing data
- **Start task on create**: (leave this checked)

![AWS DMS Tasks - Create Task (Continued)](images/step/aws_dms_tasks/create-task-2.png)

Continue by entering the following data:

- **Target table preparation mode**: Drop tables on target
- **Include LOB columns in replication**: Limited LOB mode
- **Max LOB size (kb)**: 32
- **Enable logging**: selected/checked

\newpage

#### AWS DMS Tasks - Add Selection Criteria

Add the following selection criteria, as shown below:

![AWS DMS Tasks - Add Selection Criteria](images/step/aws_dms_tasks/create-task-5.png)

\newpage

#### AWS DMS Tasks - Create Task (Final)

Review the information and click the **Create Task** button to continue.

![AWS DMS Tasks - Create Task (Final)](images/step/aws_dms_tasks/create-task-6.png)

You will now see the new DMS Task listed with a status of Creating, then Starting, then Running, as shown below

![AWS DMS Tasks - List Tasks (Updated)](images/step/aws_dms_tasks/list-tasks-status-starting.png)

---

You have now successfully set up all the major components for a database migration with AWS DMS. Next, we will troubleshoot some errors that commonly occur during real-world migrations.

---