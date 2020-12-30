# Data Engineer Test Instructions
🙃

This task is designed to test your technical proficiency with data engineering, Python and containers.

**You needn’t complete the entire test but the more you complete, the easier it will be for us to get a good idea of your skill set.**

This task is going to expire in a few days. Check the expiration date and let us know if you’re going to need more time.

❗ Before you start, read through the following:

- **Fork this repository** into your own **private** repository and don’t forget that all of the  changes you make should be done in your own fork;
- Comments are welcome because they illustrate your thinking. Please leave them under the **Additional Notes** section;
- When you’re ready, share your repository with us (Members -> Invite Member). Our handles: @annatn, @marton.hubay, @gabor.toth1, @rmokk;
- Grant our users Reporter role;
- Reply to our email providing a link to the repository we need to check

 
Send us questions if you have any. We’re looking forward to reviewing your task. Good luck! 🚀

# TEST
The primary purpose of this test is to write a data pipeline that can answer specific business questions.

💡 _Hint_: Reading through the tasks, you might decide to change your approach. So, it’s a good idea to **read the entire document before you start**.

Feel free to write the data pipeline in pure Python code or use a framework such as [dbt](https://docs.getdbt.com/) or [Dataform](https://docs.dataform.co/). 


0. **Business Questions** 🤔

- We’ve noticed that there’s something wrong with the event logging: it sometimes logs a wrong user_id which does not even exist in our database. We suspect that the problem is only related to some event types. List the event types where the problem occurs the most often.
- We have spotted that we’ve had a lot of events duplicated on a specific date. What date was that?
- What country do most of our website visitors come from?
- Our most valuable users are the ones who have completed a minimum of 5 VIEWs and 10 CLICKs. What age group do they fall in: 18-49 or 50-80? 

Once you've developed and run your pipeline, please explore the resulting data and give your answer under the Answers section.

1. **Load data in a database**
Look under the `dataset` folder. The `tables.sql` file contains the `create table` statements while the csv files contain data for each of the two tables.
Load the datasets in **Postgres**. Use a public docker image to have a local copy of your database and make sure the pipeline runs against it.

- Initialize the necessary table(s)
- Load data into the table(s)


2. **Additional Pipeline Steps**
Write additional steps to be able to answer the business questions above. When developing your pipeline, consider the following:

- It should be able to run locally for development purposes;
- It should be structured in a way that is easily extensible;
- It should be developed with repeatability in mind.

3. **Orchestrate your data pipeline**
Use an orchestrator of your choice to run the steps of your pipeline. [Airflow](https://airflow.apache.org/docs/stable/start.html) or [Prefect](https://docs.prefect.io/core/getting_started/installation.html) are really good choices but feel free to use whatever you are comfortable with. Here, you need to:

- Structure your pipeline into appropriate steps;
- Run the pipeline using the orchestrator.


4. **Use docker-compose to spin up the local environment**
Write a `docker-compose` file in order to have your environment up and running. The `docker-compose` file should spin-up:

- The Postgres database instance;
- The orchestrator with your pipeline ready to run.

**Additional considerations**
When we assess your work, we’re also going to consider:

✅ How credentials are managed and how easily the pipeline can be deployed in different environments (dev, test, prod);

✅ If the git commit messages show a good understanding of what has happened during development.


# Answers

# Additional Notes
