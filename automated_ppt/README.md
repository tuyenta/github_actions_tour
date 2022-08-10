A simple and free solution to build an architecture that can automatically extract data,
generate PowerPoint report and send it as an email attachment to user.

**Prerequisites:**

- Firstly, let’s walk through the required resources:
AWS RDS database (Feel free to choose other alternatives) that is regularly updated. This is essential, if our database is static, the generated report will be the same for every day.
- Python3 (libraries we will use: psycopg2 , pendulum , pandas and python-pptx )
- Github
- Microsoft Powerpoint

**Architecture:**

The workflow is illustrated in the below diagram:

https://miro.medium.com/max/1400/1*TcvDy3YbjG9weLgXYd4P7A.png

**Step-by-step:**
- Step 1 —create a Python script to to retrieve data from the RDS database and store results in a staging folder.
- Step 2 — Then, staging data will be pre-processed and converted into a PowerPoint report.
- Step 3 — Once the report is ready, we run a script to send email to user(s) that includes the report attached (s).
- Step 4 — After the local test is completed , create a Github workflow folder in our working repository and push new changes to Github to schedule tasks to execute every day.