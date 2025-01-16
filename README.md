# AWS Stock Market Data Analysis Pipeline
 This project demonstrates how to build a scalable and real-time data pipeline using Apache Kafka. The pipeline ingests, processes, and visualizes stock market data, highlighting core skills in distributed systems, data engineering, and cloud computing.

## Key Features:

Producer: Sends real-time stock market data to a Kafka topic.

Consumer: Consumes the data from the topic and processes it for analysis.

AWS Integration: Deploys Kafka on an EC2 instance, ensuring scalability and accessibility.

Python Integration: Utilizes Python libraries such as kafka-python for producer and consumer implementations.

## Architecture:

Producer: Connects to Kafka broker. Sends messages in JSON format containing stock data (e.g., ticker, price, timestamp). Configured with a custom value_serializer for data serialization.

Kafka Broker: Hosted on AWS EC2. Handles message distribution across topics.

Consumer: Subscribes to the Kafka topic. Processes and logs messages for downstream analysis.

## Setup Instructions:

### Prerequisites:
Before setting up, ensure you have the following:

Python: Installed with libraries such as kafka-python.

Java: Required for running Kafka.

AWS EC2 Instance: Configured and accessible for deploying Kafka.

Kafka Distribution: Downloaded and ready to install.

### Kafka Installation

Download Kafka on your EC2 instance. Start Zookeeper:

    bin/zookeeper-server-start.sh config/zookeeper.properties

Start Kafka:

    bin/kafka-server-start.sh config/server.properties

### Create Kafka Topic

Create a topic named demo_testing2:

    create --topic demo_testing2 --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1

### Testing

Start the producer and send a test message.

Run the consumer and verify the message appears in the console.

## Skills Demonstrated:

Distributed Systems: Implemented a scalable data pipeline using Kafka.

Python Development: Leveraged Python for producer and consumer functionality.

Cloud Computing: Deployed Kafka on AWS EC2 and managed its lifecycle.

Real-Time Data Processing: Designed and tested a real-time messaging system for stock market data.


   
