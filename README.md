# build_test2 - dbt Project

Welcome to the **build_test2** dbt project! This project uses **dbt** to transform and manage data in **Snowflake**, creating a reliable and reusable data pipeline for analytics and reporting.

---

## 📝 Project Overview

The `build_test2` project is designed to streamline data transformations and modeling in Snowflake. With dbt, we:
- Build models using SQL-based transformations
- Manage dependencies and test data quality
- Optimize Snowflake data workflows
- Empower analytics with clean, versioned data

## 📁 Project Structure

Here’s a quick look at the directory structure:

```
build_test2/
├── models/                    # Contains all dbt models
├── snapshots/                 # Snapshot definitions for data auditing
├── tests/                     # Custom tests for data validation
├── analyses/                  # Additional SQL analyses
├── macros/                    # Custom macros for reusable SQL snippets
├── seeds/                     # Seed files for static reference data
├── dbt_project.yml            # Project configuration
└── profiles.yml               # Connection details and profile configurations
```

---

## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed:

- [Python](https://www.python.org/downloads/)
- [dbt](https://docs.getdbt.com/dbt-cli/installation) (data build tool)
- [Snowflake account](https://www.snowflake.com/)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/build_test2.git
   cd build_test2
   ```

2. **Set up a virtual environment**:
   ```bash
   python -m venv dbt_env
   source dbt_env/bin/activate   # On Windows: dbt_env\Scripts\activate
   ```

3. **Install dbt dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure Profiles**:
   - Add your Snowflake credentials to `profiles.yml` or set environment variables as needed.
   - Ensure the profile name in `dbt_project.yml` matches the one in `profiles.yml`.

---

## 🔧 Usage

### Running dbt Commands

- **Run all models**:
  ```bash
  dbt run
  ```

- **Test data quality**:
  ```bash
  dbt test
  ```

- **View lineage and dependencies**:
  ```bash
  dbt docs generate
  dbt docs serve
  ```

- **Refresh snapshots**:
  ```bash
  dbt snapshot
  ```

### Environment Variables

For security, sensitive information such as your Snowflake account ID, user, password, and warehouse should be stored as environment variables. Example setup in PowerShell:

```powershell
$env:SNOWFLAKE_ACCOUNT = "your_account_id"
$env:SNOWFLAKE_USER = "your_username"
$env:SNOWFLAKE_PASSWORD = "your_password"
$env:SNOWFLAKE_DATABASE = "your_database"
$env:SNOWFLAKE_WAREHOUSE = "your_warehouse"
```

---

## 🛠️ Features

- **Data Transformation**: Transform raw data into usable models for analytics
- **Testing & Quality Assurance**: Ensure data quality with built-in dbt tests and custom tests
- **Snapshotting**: Maintain historical records with dbt snapshots
- **Documentation**: Auto-generate documentation and lineage graphs for transparency and collaboration
