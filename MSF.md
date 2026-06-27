### What is Microsoft Fabric?

Microsoft Fabric is an all-in-one cloud-based data analytics platform
by Microsoft that helps organizations collect, store, process, analyze,
and visualize data from a single unified environment.

                Microsoft Fabric
                       │
        ┌──────────────┴──────────────┐
        │        Compute Layer        │
        │─────────────────────────────│
        │ • Data Factory              │
        │ • Data Engineering          │
        │ • Warehouse                 │
        │ • Data Science              │
        │ • Power BI                  │
        └──────────────┬──────────────┘
                       │
                       ▼
               OneLake (Storage)
             Delta Parquet Format

---

| Components                  | Simple Meaning        | Main Purpose                  |
| -------------------------- | --------------------- | ------------------------------ |
| **OneLake**                | One storage           | Store all data                 |
| **Data Factory**           | Data mover            | ETL (Extract, Transform, Load) |
| **Lakehouse**              | Flexible storage      | Store all data types           |
| **Data Warehouse**         | Organized database    | SQL reporting                  |
| **Data Engineering**       | Build data pipelines  | Prepare and process data       |
| **Data Science**           | AI & Machine Learning | Predictions and models         |
| **Real-Time Intelligence** | Live analytics        | Analyze streaming data         |
| **Power BI**               | Dashboard tool        | Reports and visualizations     |
| **Pipeline**               | Automation            | Schedule workflows             |
| **Notebook**               | Coding workspace      | Python, SQL, Spark             |
| **Spark**                  | Processing engine     | Fast big data processing       |
| **SQL Endpoint**           | SQL access            | Query data with SQL            |

---

# 1. OneLake 🗂️ (Storage)

### What is it?

OneLake is the **central storage** for Microsoft Fabric.


### Example

A company stores:

* Customer Data
* Sales Data
* Employee Data
* Product Data

Everything is stored inside **OneLake**.

 **OneLake = One Storage**

---

# 2. Data Factory 🔄 (Move Data)

### What is it?

Data Factory collects data from different sources and prepares it for use.

This process is called **ETL**.

### ETL

**Extract**

* Collect data

↓

**Transform**

* Clean data
* Remove duplicates
* Fix errors

↓

**Load**

* Store data in OneLake

### Example

Data comes from:

* Excel
* SQL Database
* Website
* CSV File

Data Factory combines everything into one clean dataset.

**Memory Trick:** **Data Factory = Data Mover**

---

# 3. Lakehouse 🏞️

### What is it?

A Lakehouse combines the features of:

* Data Lake
* Data Warehouse

It can store:

* Images
* Videos
* CSV
* Excel
* JSON
* Structured data

### Example

Netflix stores:

* Movies
* User ratings
* Watch history
* Posters

All these different types of data can be stored in a Lakehouse.

 **Lakehouse = Store Everything**

---

# 4. Data Warehouse 🏢

### What is it?

A Data Warehouse stores **organized and structured data** for reporting.

### Example

Sales table

| Product | Price   |
| ------- | ------- |
| Laptop  | ₹60,000 |
| Mobile  | ₹25,000 |

Perfect for creating reports.

 **Warehouse = Organized Tables**

---

# 5. Data Engineering ⚙️

### What is it?

Data Engineering is the process of building systems that collect, clean, and prepare data.

Data Engineers create pipelines that move data automatically.

### Example

Every night:

* Read Excel
* Clean data
* Store in OneLake

Automatically.

### Tools used

* Notebooks
* Spark
* Pipelines

 **Data Engineering = Build Data Pipelines**

---

# 6. Data Science 🤖

### What is it?

Data Science uses data to build AI and Machine Learning models.

### Example

Predict:

* House prices
* Customer purchases
* Loan approval
* Sales forecasting

### Tools

* Python
* Machine Learning
* Notebooks

 **Data Science = Predict Future**

---

# 7. Real-Time Intelligence ⚡

### What is it?

Analyzes data immediately after it is generated.

### Example

Uber

Driver location changes every second.

Microsoft Fabric analyzes it instantly.

Other examples:

* Live stock prices
* Live sensor data
* Live website visitors

 **Real-Time = Instant Data**

---

# 8. Power BI 📊

### What is it?

Power BI converts data into beautiful reports and dashboards.

Instead of reading thousands of rows, managers see charts.

### Example

Sales

| Month | Sales |
| ----- | ----- |
| Jan   | ₹2L   |
| Feb   | ₹3L   |

Power BI creates a graph automatically.

### Charts

* Bar Chart
* Pie Chart
* Line Chart
* Dashboard
* KPI Cards

 **Power BI = Visual Reports**

---

# 9. Pipelines 🚀

### What is it?

Pipelines automate tasks.

Instead of doing work manually every day, Pipelines perform it automatically.

### Example

Every day at 9 AM:

* Read Excel
* Clean data
* Store in OneLake
* Refresh Power BI

Automatically.

 **Pipeline = Automation**

---

# 10. Notebooks 📓

### What is it?

A Notebook is where developers write code.

Mostly used with:

* Python
* SQL
* Spark

### Example

```python
print("Hello Fabric")
```

or

```sql
SELECT * FROM Sales
```

Used for data cleaning and analysis.

 **Notebook = Coding Area**

---

# 11. Spark ⚡

### What is it?

Spark is a powerful engine for processing huge amounts of data very quickly.

### Example

Instead of processing 1 GB of data,

Spark can process **terabytes or petabytes** across many computers.

 **Spark = Fast Big Data Processing**

---

# 12. SQL Endpoint 🗃️

### What is it?

Allows you to query Fabric data using SQL.

Example:

```sql
SELECT *
FROM Sales
WHERE Amount > 5000;
```

No need to move data elsewhere.

 **SQL Endpoint = Query Data with SQL**

---

# Complete Microsoft Fabric Workflow

```
text
Excel
CSV
API
SQL Database
Website
IoT Devices
      │
      ▼
Data Factory
(Collect + Clean)
      │
      ▼
OneLake
(Store Everything)
      │
      ├────────► Lakehouse
      │
      ├────────► Warehouse
      │
      ├────────► Data Engineering
      │
      ├────────► Data Science
      │
      ├────────► Real-Time Intelligence
      │
      ▼
Power BI
(Dashboards & Reports)
      │
      ▼
Business Decisions

```


