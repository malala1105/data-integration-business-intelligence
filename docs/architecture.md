# Technical Architecture

## 1. Architecture Overview

The project follows a data integration workflow designed to transform structured source files into information suitable for database storage and business intelligence analysis.

The architecture is organized into five main layers:

1. Source layer
2. Data preparation layer
3. ETL layer
4. Database layer
5. Analytics and reporting layer

Each layer performs a specific role in the overall data processing pipeline.

## 2. Data Flow

The general data flow is illustrated below:

**Excel Files → Python/Pandas → Talend Open Studio → Oracle Database → SQL & Wise Intelligence**

### 2.1 Source Layer

**Input:** Monthly Excel files.

This layer contains the original structured data used as input for the integration process.

The files are the starting point of the workflow.

### 2.2 Data Preparation Layer

**Technology:** Python and Pandas.

This layer prepares the source data before integration.

Its responsibilities include:
- Reading structured Excel files.
- Cleaning and standardizing values.
- Harmonizing data formats.
- Preparing datasets for subsequent processing.

**Output:** Prepared datasets.

### 2.3 ETL Layer

**Technology:** Talend Open Studio.

This layer manages the data integration process.

Its main responsibilities are:
- Extracting prepared data.
- Applying the required transformations.
- Loading processed records into the database environment.

**Output:** Integrated data ready for database storage.

### 2.4 Database Layer

**Technology:** Oracle Database.

This layer stores the integrated data in a centralized relational database environment.

It provides the foundation for SQL queries, data verification, and analytical use.

### 2.5 Analytics and Reporting Layer

**Technologies:** SQL and Wise Intelligence.

This final layer makes the integrated data available for analytical purposes.

It involves:
- Checking data integration through SQL queries.
- Verifying data consistency and completeness.
- Supporting the development of analytical indicators.
- Presenting information through business intelligence visualizations and dashboards.

## 3. Component Responsibilities

| Component | Main Responsibility |
|---|---|
| Excel | Source data |
| Python / Pandas | Data preparation |
| Talend Open Studio | ETL processing |
| Oracle Database | Data storage |
| SQL | Data verification and querying |
| Wise Intelligence | Analytics and visualization |

## 4. Technical Design Considerations

The workflow is based on several important principles:

- **Separation of responsibilities:** Each component has a clearly defined role.
- **Data quality:** Data preparation and validation help improve consistency.
- **Structured integration:** ETL processing organizes the movement of data between stages.
- **Analytical readiness:** Integrated data are made available for reporting and analysis.

## 5. Confidentiality

This documentation intentionally presents the architecture at a generic technical level.

No confidential datasets, internal database schemas, production configurations, connection credentials, or operational details are disclosed.