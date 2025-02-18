# Change Data Capture (CDC) with Debezium, Kafka, PostgreSQL, and Docker 

## Overview

This project demonstrates a Change Data Capture (CDC) pipeline using Debezium, Kafka, and PostgreSQL, all orchestrated with Docker. The Python script included in this repository generates simulated financial transactions and inserts them into a PostgreSQL database. This setup is ideal for testing and understanding CDC workflows in a controlled environment.

The script leverages the faker library to create realistic, fictitious transaction data, which is then inserted into a PostgreSQL table. Debezium captures these changes and streams them to Kafka for further processing or analysis.

## System Architecture
![system architecture.png](architecture.png)

## Prerequisites

Before running this script, ensure you have the following installed:
- Python 3.10+
- `psycopg2` library for Python
- `faker` library for Python
- PostgreSQL server running locally or accessible remotely
- Docker and Docker Compose installed on your machine.
- Basic understanding of Docker, Kafka, and Postgres.

## Installation

1. **Install Required Python Libraries:**

   You can install the required libraries using pip:

   ```bash
   pip install psycopg2-binary faker
   ```

## Services in the Compose File

- **Zookeeper:** A centralized service for maintaining configuration information, naming, providing distributed synchronization, and providing group services.
- **Kafka Broker:** A distributed streaming platform that is used here for handling real-time data feeds.
- **Confluent Control Center:** A web-based tool for managing and monitoring Apache Kafka.
- **Debezium:** An open-source distributed platform for change data capture.
- **Debezium UI:** A user interface for managing and monitoring Debezium connectors.
- **Postgres:** An open-source relational database.

5. **Accessing the Services:**
   - Kafka Control Center is accessible at `http://localhost:9021`.
   - Debezium UI is accessible at `http://localhost:8080`.
   - Postgres is accessible on the default port `5432`.
