Data pipelines define a sequence of activities that orchestrate an overall process, usually by extracting data from one or more sources and loading it into a destination; often transforming it along the way. Pipelines are commonly used to automate extract, transform, and load (ETL) processes that ingest transactional data from operational data stores into an analytical data store, such as a lakehouse, data warehouse, or SQL database.

If you're already familiar with Azure Data Factory, data pipelines in Microsoft Fabric use a similar architecture of connected activities. A pipeline can include data movement, transformation, and control flow activities. You can run pipelines on demand, on a schedule, or in response to an event.


Pipelines in Microsoft Fabric encapsulate a sequence of activities that perform data movement and processing tasks. You can use a pipeline to define data transfer and transformation activities, and orchestrate these activities through control flow activities that manage branching, looping, and other typical processing logic. The graphical pipeline canvas in the Fabric user interface enables you to build complex pipelines with minimal or no coding required.

Screenshot of a pipeline in Microsoft Fabric.

Core pipeline concepts
Before building pipelines in Microsoft Fabric, you should understand a few core concepts.

Activities
Activities are the executable tasks in a pipeline. You can define a flow of activities by connecting them in a sequence. The outcome of a particular activity (success, failure, or completion) can be used to direct the flow to the next activity in the sequence.

There are three broad categories of activity in a pipeline.

Data movement activities - activities that move data between supported sources and destinations. For example, a Copy Data activity can extract data from an external source and load it into a lakehouse, warehouse, SQL database, or another supported destination.

Data transformation activities - activities that process and transform data. These activities include Dataflow Gen2 activities that run dataflows, Notebook activities that run Spark code, Stored procedure activities that run SQL code, and Delete data activities that delete existing data.

Control flow activities - activities that you can use to implement loops, conditional branching, or manage variable and parameter values. The wide range of control flow activities enables you to implement complex pipeline logic to orchestrate data ingestion and transformation flow.

 Tip

For details about the complete set of pipeline activities available in Microsoft Fabric, see Activity overview in the Microsoft Fabric documentation.

Parameters
Pipelines can be parameterized, enabling you to provide specific values to be used each time a pipeline is run. For example, you might want to use a pipeline to save ingested data in a folder, but have the flexibility to specify a folder name each time the pipeline is run.

Using parameters increases the reusability of your pipelines, enabling you to create flexible data ingestion and transformation processes.

Pipeline runs
Each time a pipeline is executed, a data pipeline run is initiated. You can start a run on demand in the Fabric user interface, on a schedule, or in response to an event. Use the unique run ID to review run details, confirm that activities completed successfully, and investigate the settings used for each execution.

Pipelines in Microsoft Fabric encapsulate a sequence of activities that perform data movement and processing tasks. You can use a pipeline to define data transfer and transformation activities, and orchestrate these activities through control flow activities that manage branching, looping, and other typical processing logic. The graphical pipeline canvas in the Fabric user interface enables you to build complex pipelines with minimal or no coding required.

Screenshot of a pipeline in Microsoft Fabric.

Core pipeline concepts
Before building pipelines in Microsoft Fabric, you should understand a few core concepts.

Activities
Activities are the executable tasks in a pipeline. You can define a flow of activities by connecting them in a sequence. The outcome of a particular activity (success, failure, or completion) can be used to direct the flow to the next activity in the sequence.

There are three broad categories of activity in a pipeline.

Data movement activities - activities that move data between supported sources and destinations. For example, a Copy Data activity can extract data from an external source and load it into a lakehouse, warehouse, SQL database, or another supported destination.

Data transformation activities - activities that process and transform data. These activities include Dataflow Gen2 activities that run dataflows, Notebook activities that run Spark code, Stored procedure activities that run SQL code, and Delete data activities that delete existing data.

Control flow activities - activities that you can use to implement loops, conditional branching, or manage variable and parameter values. The wide range of control flow activities enables you to implement complex pipeline logic to orchestrate data ingestion and transformation flow.

 Tip

For details about the complete set of pipeline activities available in Microsoft Fabric, see Activity overview in the Microsoft Fabric documentation.

Parameters
Pipelines can be parameterized, enabling you to provide specific values to be used each time a pipeline is run. For example, you might want to use a pipeline to save ingested data in a folder, but have the flexibility to specify a folder name each time the pipeline is run.

Using parameters increases the reusability of your pipelines, enabling you to create flexible data ingestion and transformation processes.

Pipeline runs
Each time a pipeline is executed, a data pipeline run is initiated. You can start a run on demand in the Fabric user interface, on a schedule, or in response to an event. Use the unique run ID to review run details, confirm that activities completed successfully, and investigate the settings used for each execution.

Pipelines in Microsoft Fabric encapsulate a sequence of activities that perform data movement and processing tasks. You can use a pipeline to define data transfer and transformation activities, and orchestrate these activities through control flow activities that manage branching, looping, and other typical processing logic. The graphical pipeline canvas in the Fabric user interface enables you to build complex pipelines with minimal or no coding required.

Screenshot of a pipeline in Microsoft Fabric.

Core pipeline concepts
Before building pipelines in Microsoft Fabric, you should understand a few core concepts.

Activities
Activities are the executable tasks in a pipeline. You can define a flow of activities by connecting them in a sequence. The outcome of a particular activity (success, failure, or completion) can be used to direct the flow to the next activity in the sequence.

There are three broad categories of activity in a pipeline.

Data movement activities - activities that move data between supported sources and destinations. For example, a Copy Data activity can extract data from an external source and load it into a lakehouse, warehouse, SQL database, or another supported destination.

Data transformation activities - activities that process and transform data. These activities include Dataflow Gen2 activities that run dataflows, Notebook activities that run Spark code, Stored procedure activities that run SQL code, and Delete data activities that delete existing data.

Control flow activities - activities that you can use to implement loops, conditional branching, or manage variable and parameter values. The wide range of control flow activities enables you to implement complex pipeline logic to orchestrate data ingestion and transformation flow.

 Tip

For details about the complete set of pipeline activities available in Microsoft Fabric, see Activity overview in the Microsoft Fabric documentation.

Parameters
Pipelines can be parameterized, enabling you to provide specific values to be used each time a pipeline is run. For example, you might want to use a pipeline to save ingested data in a folder, but have the flexibility to specify a folder name each time the pipeline is run.

Using parameters increases the reusability of your pipelines, enabling you to create flexible data ingestion and transformation processes.

Pipeline runs
Each time a pipeline is executed, a data pipeline run is initiated. You can start a run on demand in the Fabric user interface, on a schedule, or in response to an event. Use the unique run ID to review run details, confirm that activities completed successfully, and investigate the settings used for each execution.


he Copy Data activity moves data between supported data stores as part of a pipeline. For example, you can use it to ingest data from an external source into a lakehouse file or table before other pipeline activities process the data.

You can combine the Copy Data activity with other activities to create a repeatable data ingestion process. For example, use a Delete data activity to remove existing data, a Copy Data activity to replace the data from an external source, and a Notebook activity to transform the data and load it into a table.

The Copy Data tool
Screenshot of the Copy Data tool in Microsoft Fabric.

When you add a Copy Data activity to a pipeline, a graphical tool takes you through the steps required to configure the data source and destination for the copy operation. A wide range of source connections is supported, making it possible to ingest data from most common sources. In OneLake, this includes support for lakehouse, warehouse, SQL Database, and others.

Screenshot of the Copy Data tool showing the SQL Database support in Microsoft Fabric.

Copy Data activity settings
After you've added a Copy Data activity to a pipeline, you can select it in the pipeline canvas and edit its settings in the pane underneath.

Screenshot of a Copy Data activity in Microsoft Fabric.

When to use the Copy Data activity
Choose a data movement option based on how you need to process and orchestrate the data.

Option	Use when
Copy job	You need a simplified experience for a copy-only workload, including bulk, incremental, or change data capture movement.
Copy Data activity	You need to move data as one step in a pipeline or require detailed control over the copy operation.
Dataflow Gen2 activity	You need to transform data with Power Query or combine data from multiple sources.
When you use a Copy Data activity, you can apply transformations in later pipeline activities. For example, add a Dataflow Gen2 activity to run a dataflow that contains multiple Power Query transformation steps.


Use pipeline templates
Completed
100 XP
1 minute
Choose your preferred content format
You can combine activities to create custom data ingestion and transformation processes. For common scenarios, Microsoft Fabric includes predefined pipeline templates that you can configure and customize.

Start with a predefined template
To create a pipeline based on a template, select the Templates tile in a new pipeline as shown here.

Screenshot of the Choose a task to start tile.

Selecting this option displays a selection of pipeline templates, as shown here.

Screenshot of the pipeline template gallery in Microsoft Fabric.

You can select the most appropriate template for your needs, and then edit the pipeline in the pipeline canvas to customize it to your needs.

Reuse a custom pipeline template
The template gallery also supports custom pipeline templates. To reuse a pipeline, select Export on the Home tab to save the pipeline as a .zip template file. You can then import the file from the Home tab or select Import template in the template gallery.

When you import a template, review its activities and select the required connections before you use it. This approach helps you apply a consistent pipeline structure across workspaces while keeping connection settings specific to each environment.

Run and monitor pipelines
Completed
100 XP
2 minutes
Choose your preferred content format
After you complete a pipeline, use Validate to check its configuration. You can then run the pipeline on demand, add one or more schedules, or configure an event trigger.

Screenshot of the run options for a pipeline in Microsoft Fabric.

Choose how to start a pipeline
Fabric supports three ways to start a pipeline run:

On-demand run: Select Run on the Home tab to start the pipeline immediately. Fabric prompts you to save changes before the run starts.
Scheduled run: Select Schedule to define when the pipeline runs. A schedule includes start and end dates, a frequency, and a time zone. A pipeline can have multiple schedules.
Event-based run: Select Trigger to start the pipeline in response to file, job, or workspace events. For example, a storage event can start a pipeline when a file arrives in OneLake or Azure Blob Storage.
Pipeline parameters let you pass values for each run. For scheduled runs, the parameter names in the schedule must match the parameter names defined in the pipeline.

View run history
You can view recent runs from the pipeline canvas or select View run history from the pipeline item in the workspace. Run history displays the status of each run. Select a run to review its run ID, activity durations, inputs, outputs, and error details.

Screenshot of a pipeline run history in Microsoft Fabric.

For a broader view, select Go to monitor to open the Monitoring hub. There, you can filter pipeline and activity runs, export monitoring data, and open performance details. The Gantt view helps you compare run durations and identify delays or overlapping runs.

When a run fails, use its activity details to investigate the error. After you correct the issue, you can rerun the entire pipeline or rerun from the failed activity.





exercise :- https://microsoftlearning.github.io/mslearn-fabric/Instructions/Labs/04-ingest-pipeline.html


With Microsoft Fabric, you can create pipelines that orchestrate data movement, transformation, and control flow activities. You can start pipelines on demand, on a schedule, or in response to an event, and use run history and the Monitoring hub to investigate each execution.

