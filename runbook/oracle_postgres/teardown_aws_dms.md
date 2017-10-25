## Teardown AWS DMS Resources

You will now destroy the previously created AWS DMS resources. Because there is an interdependency between these resources, we will terminate the resources in the reverse order of the original creation.

The order for destruction will be:

- Tasks
- Endpoints
- Replication Instances

You can find all of these resources under the AWS console for AWS Database Migration Services at the following link:

> <http://amzn.to/aws-tokyo-dms-instances>
(=> <https://ap-northeast-1.console.aws.amazon.com/dms/home?region=ap-northeast-1#replication-instances:>)

### Teardown AWS DMS Resoures: Tasks

First, you will delete the existing AWS DMS Task associated with this workshop. You can find this at the following link:

> <http://amzn.to/aws-tokyo-dms-tasks>
(=> <https://ap-northeast-1.console.aws.amazon.com/dms/home?region=ap-northeast-1#tasks:>)

You should see a lit of all DMS Tasks in this region. Locate the DMS Task created earlier during this workshop. The default name for the Task created during this workshop was **dms-workshop-task-oracle2postgres**.

Select the task and, if it is running, click the **Stop** button.

Wait a few moments until the Task until the status is updated to Stop, then click the **Delete** button.

---

The process of deleting a DMS Task may take a minute or two. Continue to refresh until the DMS Task is no longer visible, then proceed to the next step.

---

### Teardown AWS DMS Resoures: Endpoints

Next, you can now delete the DMS Endpoints that were created earlier in this lab. You can find this at the following link:

> <http://amzn.to/aws-tokyo-dms-endpoints> (=> <https://ap-northeast-1.console.aws.amazon.com/dms/home?region=ap-northeast-1#endpoints:>)

You should now see a list of all DMS Endpoints in this region. There will be two Endpoints to delete, one for the Source and one for the Target. The default names for this workshop are:

- Source: **dms-workshop-oracle**
- Target: **dms-workshop-postgres**

If you used those defaults, your page should look like the following:

![Teardown AWS DMS - List All Endpoints](images/teardown/aws_dms/endpoint-all.png)

Select the Source Endpoint as shown below, then click the **Delete** button.

![Teardown AWS DMS - Select Source Endpoint](images/teardown/aws_dms/endpoint-source.png)

You will be prompted to confirm this deletion as shown below, if you are certain this is the correct Endpoint from the workshop, then click the **Delete** button.

![Teardown AWS DMS - Delete Source Endpoint](images/teardown/aws_dms/endpoint-source-delete.png)

Next, select the Target Endpoint as shown below -- alson note that the status for the Source Endpoint should now display as **Deleting**.

![Teardown AWS DMS - Select Target Endpoint](images/teardown/aws_dms/endpoint-target.png)

Once selected, repeat the process as above, clicking the **Delete** button and confirming that you wish to delete the Target Endpoint from this workshop. Finally, you will see the following page:

![Teardown AWS DMS - Endpoints Deleted](images/teardown/aws_dms/endpoint-deleted.png)

---

The process of deleting DMS Endpoints may take a minute or two. Continue to refresh until the DMS Endpoints are no longer visible, then proceed to the next step.

---

### Teardown AWS DMS Resoures: Replication Instances

To delete the DMS replication instances for this workshop, we will first view the console for replication instances by visiting the following link:

> <http://amzn.to/aws-tokyo-dms-instances>
(=> <https://ap-northeast-1.console.aws.amazon.com/dms/home?region=ap-northeast-1#replication-instances:>)

You should see a lit of all DMS Replication Instances in this region.

![Teardown AWS DMS - Replication Instance List](images/teardown/aws_dms/repl-inst-list.png)

Locate the DMS Replication Instance created earlier during this workshop. The default name for the Replication Instance created during this workshop was **dms-workshop-oracle2postgres-repl**.

You will now select your workshop DMS Replication Instance, clicking the **Delete** button to proceed:

![Teardown AWS DMS - Replication Instance Selected](images/teardown/aws_dms/repl-inst-selected.png)

You will receive the following confirmation:

![Teardown AWS DMS - Replication Instance Confirm Deletion](images/teardown/aws_dms/repl-inst-delete.png)

Click the **Delete** button again if you certain this is the correct DMS Replication Instance you set up earlier in the workshop.

The status of the Replication Instance will now show as **Deleted**:
![Teardown AWS DMS - Replication Instance Deleted](images/teardown/aws_dms/repl-inst-deleted.png)

---

The process of deleting DMS Replication Instances may take a minute or two. Continue to refresh until the DMS Replication Instances are no longer visible, then proceed to the next step.

---