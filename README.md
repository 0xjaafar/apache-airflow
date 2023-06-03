# Apache Airflow Docker Compose Setup

This repository provides a Docker Compose setup for Apache Airflow. Follow the steps below to get started.

## Prerequisites

- Docker installed on your system

## Installation

1. Download the `docker-compose.yaml` file by running the following command:
```curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.4.1/docker-compose.yaml'```

2. Create the necessary directories by running the following command:
```mkdir ./dags ./logs ./plugins```


3. Create an environment file. Run the appropriate command based on your operating system:
- Ubuntu / Mac OSX:
  ```
  touch .env
  ```
- Windows (PowerShell):
  ```
  ni .env
  ```

4. Set the `AIRFLOW_UID` environment variable by running the following command:
echo -e "AIRFLOW_UID=$(id -u)" > .env


## Usage

To start the Apache Airflow containers, run the following command:
``` docker-compose up airflow-init ```