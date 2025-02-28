Overview
========

This project was created using the Astronomer CLI with the command astro dev init. Below, you'll find an overview of the project's structure and instructions on how to run Apache Airflow locally.

Project Contents
================

Your Astronomer project includes the following files and directories:

dags/ – This is where your Airflow DAGs (workflows) live. By default, there's an example DAG:

example_astronauts.py – A simple ETL pipeline that fetches a list of astronauts in space from the Open Notify API and prints their names. This DAG demonstrates the TaskFlow API and dynamic task mapping. Check out the Getting Started tutorial (https://www.astronomer.io/docs/learn/get-started-with-airflow)for more details.

Dockerfile – Defines the Astro Runtime Docker image for your project. You can customize it to add additional dependencies or configurations.

include/ – A folder for any extra files you want to use in your project. It's empty by default.

packages.txt – A place to list any OS-level packages your project needs. Empty by default.

requirements.txt – A file where you can list Python dependencies needed for your project. Empty by default.

plugins/ – If you want to add custom or community Airflow plugins, place them here. Empty by default.

airflow_settings.yaml – Allows you to define Airflow Connections, Variables, and Pools locally instead of setting them manually in the Airflow UI.



Deploy Your Project Locally
===========================

To start Airflow on your local machine, simply run:
**astro dev start**

This will spin up four Docker containers:

Postgres – Stores Airflow’s metadata

Webserver – Hosts the Airflow UI

Scheduler – Monitors and triggers tasks

Triggerer – Handles deferred tasks

You can verify that everything is running by checking your active Docker containers:
docker ps

Accessing the Airflow UI

Once everything is running, open your browser and go to: http://localhost:8080/

Log in with:

Username: admin

Password: admin

Connecting to the Postgres Database
If needed, you can access the Postgres database at: localhost:5432/postgres
