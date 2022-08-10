A simple and free solution to automate the processing of crawling data, storing records
in database and converting them to meaningful dashboards for your personal need.

**Prerequisites:**

- Python3 (used libraries: Scrapy, apscheduler, pg8000)
- Docker (2 containers: 1 for running application, 1 for visualization with Apache Superset)
- AWS EC2 (free tier)
- AWS RDS (free tier)
- DBeaver

**Architecture:**

The workflow is illustrated in the below diagram:

https://miro.medium.com/max/1400/1*vtADEDTc8gLzDPTIc4j9oQ.png

**Step-by-step:**
- Step 1: Crawling data with Scrapy
- Step 2: Build a scheduler
- Step 3: Store data in RDS
- Step 4: Build a Docker image
- Step 5: Visualize with Apache Superset