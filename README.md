# ⚙️ Automating Spark Data Transformations with Notebooks and Pipelines in Azure Synapse

## Overview

In this assignment, I ran a **Spark notebook interactively** and then encapsulated it within an **Azure Synapse pipeline** to automate a **data transformation process** from CSV to Parquet. This end-to-end exercise gave me a solid understanding of both **interactive data development** and **automated orchestration** in Synapse Studio.

## 🧠 What I Did

### ✅ Interactive Notebook Execution

- Connected to my Azure Synapse workspace and attached a Spark pool
- Imported the `Spark Transform.ipynb` notebook
- Explored and previewed raw CSV sales order files from Azure Data Lake
- Executed notebook cells to:
  - Set a unique output folder name using `RunId`
  - Load and transform sales data (split customer names, cast values, clean columns)
  - Save the results in **Parquet** format for efficient querying

### ✅ Data Validation

- Verified the creation of a uniquely named output folder in the **Data Lake**
- Queried the Parquet files using **serverless SQL** to confirm successful transformation

### ✅ Pipeline Automation

- Marked a parameter cell in the notebook to accept a `folderName` input
- Created a **Synapse pipeline** named `Transform Sales Data`
- Added a **Notebook activity** that passed the `@pipeline().RunId` to generate dynamic output paths
- Attached the activity to the Spark pool with optimized executor settings

### ✅ Monitoring and Output

- Published and triggered the pipeline manually
- Monitored pipeline execution from the **Monitor** page in Synapse Studio
- Validated successful pipeline execution and checked for Parquet output in the correct path

## 🔧 Technologies Used

- Azure Synapse Analytics  
- Apache Spark & PySpark  
- Azure Data Lake Gen2  
- Parquet Format  
- Synapse Pipelines  
- Serverless SQL Pool

## ✅ Key Takeaways

- Spark notebooks are great for **iterative development and transformation**
- You can easily **parameterize and reuse** notebooks in pipelines
- Orchestration with **Synapse pipelines** enables reliable, automated processing
- Using dynamic folder names (`@pipeline().RunId`) ensures **traceability and data separation**

---

📎 **Connect with me on Linkedin**: [https://www.linkedin.com/in/eyilan/]
