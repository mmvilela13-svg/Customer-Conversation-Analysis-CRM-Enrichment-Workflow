# Customer-Conversation-Analysis-CRM-Enrichment-Workflow
This workflow analyzes customer conversations and automatically enriches a CRM with structured information extracted from those interactions.

It is designed for a car dealership / automobile stand, where collecting, organizing, and analyzing customer information and documentation is essential for sales and compliance processes.

In addition to CRM updates, the workflow stores data for large-scale insight analysis and manages customer documentation securely.

⸻

# Key Features

## CRM Management
	•	Checks whether a customer already exists in the CRM.
	•	If the customer does not exist:
	•	Creates a new CRM record.
	•	Creates a dedicated folder for storing customer documents.
	•	Registers the customer in an analytics database for large-scale insights.

⸻

# Conversation Analysis

Messages are analyzed based on their type:

Text & Audio Messages (Conversation Data)
	•	Extracts relevant information such as:
	•	Product or vehicle of interest
	•	Customer intent
	•	Key conversation data
	•	Can be extended to analyze:
	•	Customer behavior in chat
	•	Objections
	•	Level of interest or readiness to buy

To store structured conversational insights, a JavaScript node is used to simulate AI behavior.
This allows the workflow to generate AI-like parameters and store conversation memory in PostgreSQL, ensuring consistency and control over stored data.

⸻

# Images & Documents (Documentation Data)
	•	Detects whether the received document is required for the sales or validation process.
	•	If the document is required:
	•	Extracts relevant data from it.
	•	Stores the document in the customer’s previously created folder.

From documents, the workflow can extract structured information such as:
	•	Marital status
	•	Number of dependents
	•	Income level
	•	Other legally permitted customer data

⚠️ All data extraction is performed strictly within the legal and regulatory framework.

⸻

# Data Storage & Insights
	•	CRM stores structured customer profiles.
	•	Documents are stored per customer for traceability and compliance.
	•	A separate database is used to:
	•	Aggregate customer data
	•	Analyze insights at scale
	•	Support reporting and business intelligence

⸻

# High-Level Workflow Logic
	1.	Receive customer messages and files.
	2.	Check if the customer exists in the CRM.
	3.	Create CRM record and document folder if needed.
	4.	Store customer reference in an analytics database.
	5.	Classify incoming data:
	•	Text / Audio → conversation analysis
	•	Images / Documents → document validation and extraction
	6.	Extract relevant information.
	7.	Store structured data in CRM, PostgreSQL memory, and document storage.

⸻

# Use Cases
	•	Automotive dealerships and sales stands
	•	CRM automation and enrichment
	•	Customer intent and behavior analysis
	•	Secure document collection and validation
	•	Large-scale customer insight analysis
