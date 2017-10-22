## Schema Conversion in AWS SCT

### Schema Conversion - Review Report

Review the project screen:

- Uncheck all schemas on the left-pane except for the DMS_SAMPLE schema.
- Click **Actions** > **Create Report**
- Go to the **Summary** tab on the top and review the generated report

![Schema Conversion - Review Conversion Report](images/step/aws_sct_convert_schema/schema-summary.png)

### Schema Conversion - Review and Convert Schema

On the left-hand pane, look through the schema tree of Oracle objects and note what could be automatically converted and what could not be converted.

### Schema Conversion - Convert Source Schema

Now, right-click and click **Convert Schema** as shown below:

![Schema Conversion - Source Apply (via right-click)](images/step/aws_sct_convert_schema/convert-schema-click.png)

If right-click is not availabe to you, you can also select the source database and click **Actions** > **Convert Schema** as shown below:

![Schema Conversion - Source Apply (via Actions)](images/step/aws_sct_convert_schema/convert-schema-actions.png)

### Schema Conversion - Review Target Schema

The schema will be converted and shown on the PostgreSQL instance (it has not been applied yet) as shown below:

![Schema Conversion - Target Review](images/step/aws_sct_convert_schema/convert-schema-target.png)

Take a few minutes to review the objects being converted.

Since the majority of the objects which could not be converted are secondary objects like functions or procedures, we will proceed with the migration.

### Schema Conversion - Apply Target Schema

Right click on the created schema on the right-hand panel, representing the target Postgres database, and click **Apply to database**, as shown below:

![Schema Conversion - Target Apply (via right-click)](images/step/aws_sct_convert_schema/convert-schema-target-apply.png)

If right-click is not available, then select the target database name and select **Actions** > **Apply to Database** as shown below:

![Schema Conversion - Target Apply (via Actions)](images/step/aws_sct_convert_schema/convert-schema-target-actions.png)

This will apply all those converted objects in the PostgreSQL target.

> The above steps will convert all your Oracle objects into PostgreSQL objects. Objects which could not be converted automatically must be taken care of manually after migration at a later time.