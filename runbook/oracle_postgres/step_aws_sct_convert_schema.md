## Convert Schema in AWS SCT

Review the project screen:

- Uncheck all schemas on the left except for the DMS_SAMPLE schema. 
- Click **Actions** > **Create Report**
- Go to the **Summary** tab on the top and review the generated report

![Convert Schema - Summary](images/step/aws_sct_convert_schema/schema-summary.png)

### Review and Convert Schema

On the left-hand pane, look through the schema tree of Oracle objects and note what could be automatically converted and what could not be converted.

Now, right click and click *Convert Schema* as shown below:

![Convert Schema - Execute](images/step/aws_sct_convert_schema/convert-schema-click.png)

The schema will be converted and shown on the PostgreSQL instance (it has not been applied yet) as shown below:

![Convert Schema - Target Review](images/step/aws_sct_convert_schema/convert-schema-target.png)

Take a few minutes to review the objects being converted.

Since the majority of the objects which could not be converted are secondary objects like functions or procedures, we will proceed with the migration. Right click on the created schema on the right-hand panel, representing the target Postgres database, and click **Apply to database**, as shown below:

![Convert Schema - Target Apply](images/step/aws_sct_convert_schema/convert-schema-target-apply.png)

This will apply all those converted objects in the PostgreSQL target.

> The above steps will convert all your Oracle objects into PostgreSQL objects. Objects which could not be converted automatically must be taken care of manually after migration at a later time.