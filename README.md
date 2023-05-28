### Reactive Data Streaming App with Python and Apache Kafka
This repository contains a solution that enables live notifications from services that do not support live notifications. It provides a method to watch and react to changes in various systems, such as online stores, YouTube videos, or other department systems at work, even when those systems do not have a notification API. The solution utilizes Python, Apache Kafka, ksqlDB, and Telegram to create a reactive data streaming application.

## Introduction
Have you ever wondered how to receive live notifications from services that lack native support for such functionality? This project offers a solution that brings data to life by transforming a static data source, such as YouTube's REST API, into a reactive system. The system is designed to fetch and process data using Python, stream the data into an Apache Kafka topic, analyze the incoming data with ksqlDB for important changes, and finally, send out live custom notifications via Telegram.

## Installation
To set up and run this application , follow these steps:

Clone the repository:
```bash

git clone <repository-url>
```
Install the required dependencies:
```bash
pip install -r requirements.txt
```
Configure the application:

The cluster is created in confluent
Open the config.yaml file and provide the necessary configuration values, such as API keys and schema credentials.
Start Apache Kafka.
Ensure the cluster running.
Use the sql file to create the streams and tables. 
Create a bot in telegram and use its message id in the telegram_outbox stream. 
Create a https sink connector using confluent. 

Run the application:

```bash
python youtube_watcher.py
```
## Usage
After successfully installing and running the application, it will start fetching data from the specified web API, stream it live into an Apache Kafka topic, process the incoming data using ksqlDB to identify important changes, and send out custom notifications through Telegram.

The application's functionality can be extended or modified by updating the Python code in youtube_watcher.py according to specific requirements. Additionally, the configuration file (config.yaml) allows customization of various parameters, including API credentials, Kafka settings, and notification preferences.

## Contributing
Contributions to this project are welcome! If you have any ideas, improvements, or bug fixes, please submit a pull request. Make sure to follow the existing code style and provide detailed information about the changes you propose.

## License
This project is licensed under the MIT License. Feel free to use, modify, and distribute the code as per the terms of the license.

## Acknowledgements
Special thanks to Kris Jenkins for providing the step-by-step build that inspired this project.

### Contact
If you have any questions, suggestions, or feedback, please feel free to reach out to the project maintainers or open an issue in the repository. We appreciate your interest and involvement!