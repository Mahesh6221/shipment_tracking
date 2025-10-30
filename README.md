Shipment Tracking

Project Overview
This project analyzes the journey of shipments for a logistics company. The focus is on transforming shipment tracking data to understand delivery performance and end-to-end journeys through a courier network. The solution flattens nested JSON data, computes important metrics, handles logistics edge cases, and produces CSV reports for further analysis.


Project Overview
- How to Use This Project
- Tools and Environment
- Data Source and Setup
- Project Workflow
- Final Deliverables

How to Use This Project
To use or reproduce this project, clone the repository from GitHub:

git clone https://github.com/yourusername/shipment-tracking-analysis.git


Tools and Environment
Databricks

Language: Python,Pyspark

File Format: JSON (input) → CSV (output)

Directory Structure:
- data/ (input, JSON format)
- outputs/ (processed shipment details and summary, CSV format)

Data Source and Setup
Step 1: Download the Data
Obtain the shipment tracking dataset from the assignment resource or instructor-supplied link.

Step 2: Prepare Data Directory
Place the JSON dataset file inside the data/ directory in your project root.

Step 3: Launch Your Jupyter Notebook or Python Script
Open the supplied notebook or script in your Python environment.


Project Workflow (Assignment Parts)
Part 1: Load and Explore Data
Load the shipment tracking JSON file into a pandas DataFrame.

Explore schema, row counts, examples, and nested fields.

Part 2: Flatten and Extract Shipment Data
Extract shipment-level fields: tracking number, payment type, shipment weight, pickup/drop address, and status events.

Flatten nested arrays and parse important event timestamps.

Part 3: Compute Shipment Performance Metrics
Compute human-readable IST datetimes (pickup, delivery).

Calculate days taken for delivery (pickup to delivery in days).

Count number of delivery attempts (unique 'Out for Delivery' events).

Part 4: Handle Edge Cases
Properly handle shipments with missing or duplicate events, same-day delivery, and missing values.

Part 5: Output Flattened Shipment CSV
Output: outputs/shipments_flattened.csv

Each row: one shipment, with all computed fields (tracking number, pickup/delivery datetimes, days taken, payment type, pincodes, delivery attempts, etc).

Part 6: Output Delivery Statistics Summary CSV
Output: outputs/shipment_summary.csv

Contains: mean, median, and mode for days taken for delivery and delivery attempt counts.

Final Deliverables
Python notebook or script with code, comments, and explanations
shipments_flattened.csv: per-shipment records

shipment_summary.csv: delivery performance summary