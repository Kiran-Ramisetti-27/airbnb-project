# Airbnb Data Engineering Project | Snowflake & dbt

## About This Project

I'm working on an Airbnb data engineering project using Snowflake, dbt Core, and SQL.

I'm using Airbnb listings, hosts, and reviews datasets to practice loading data into Snowflake, building dbt models, cleaning and transforming data, and preparing it for analysis.

I'm also planning to work on incremental models, snapshots, data quality tests, macros, and CI/CD as I progress through the project.

## Tools I'm Using

- Snowflake
- dbt Core
- SQL
- Python
- uv
- VS Code
- Git and GitHub

## What I've Done So Far

### Snowflake Setup
- Created the `AIRBNB` database with `RAW` and `DEV` schemas.
- Configured the `COMPUTE_WH` warehouse with auto-suspend and auto-resume.
- Loaded listings, hosts, and reviews CSV files from S3 into Snowflake using `COPY INTO`.
- Created a separate `DBT` service user and `TRANSFORM` role.
- Configured RSA public/private key authentication for connecting dbt to Snowflake.
- Set up the required Snowflake permissions.

### dbt Setup
- Installed dbt Core and the Snowflake adapter.
- Set up a Python virtual environment using uv.
- Configured `profiles.yml` and `dbt_project.yml`.
- Connected dbt Core to Snowflake.
- Set up Git and connected the project to my GitHub repository.

### dbt Models
- Created source models for listings, hosts, and reviews.
- Used `ref()` to connect models and manage dependencies.
- Started building dimension models for listings and hosts.
- Added transformations to handle missing host names, correct minimum-night values, and convert listing prices into numeric values.
- Configured source models as views and dimension models as tables.

## What I'm Planning to Do Next

- Build an incremental fact model for Airbnb reviews.
- Use dbt sources instead of directly referencing raw Snowflake tables.
- Implement incremental loading and full-refresh scenarios.
- Create additional dimension models and join listings with hosts.
- Implement dbt snapshots to track changes in listings and hosts using SCD Type 2.
- Add generic and custom data quality tests.
- Work with dbt seeds, Jinja, macros, and packages.
- Generate dbt documentation and explore model lineage.
- Build analytics marts using listings, hosts, and reviews data.
- Add GitHub Actions for automated dbt checks.
- Create a Tableau dashboard using the transformed Snowflake data.

I'll keep updating this repository as I work through each part of the project.