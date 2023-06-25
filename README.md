# ChatBot

This is a simple chatbot implementation using the ChatterBot library in Python. The chatbot is designed to engage in conversations with users, providing pre-defined responses based on the training data.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)

## Features

- **Natural Language Processing**: The chatbot utilizes natural language processing techniques to understand user input and generate appropriate responses.
- **Pre-trained Models**: The chatbot comes with pre-trained language models that provide a starting point for conversations.
- **Ready Corpus**: It's also comes with a different language corpus data, you can find it [here](https://github.com/gunthercox/chatterbot-corpus).
- **Customizable Training**: You can train the chatbot with your own conversational data to make it more specific to your use case.
- **Multiple Logic Adapters**: The chatbot supports multiple logic adapters that handle different aspects of conversation generation, such as mathematical calculations, sentiment analysis, or fallback responses.
- **Storage Adapter**: The chatbot uses a storage adapter to persist conversation data, allowing you to resume conversations and track user interactions.

## Getting Started

To get started with the chatbot, you can watch this tutorial video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/qextOtQr1Ac" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

or just follow this steps:

1. Install the necessary libraries.
```
pip install nltk chatterbot spacy
```
```
pip install --upgrade sqlalchemy
```
2. Take [sql_storage.py](sql_storage.py) file to this path.
```
[system path]\anaconda3\Lib\site-packages\chatterbot\storage
```
3. Open the notebook, you can find two separate code. One's for the customized training and the other to train using ready corpus data.
4. Feel free to post in issues if there is a problem.
5. [ChatterBot Documentation](https://chatterbot.readthedocs.io/en/stable/index.html).

## Usage

The usage of your ChatterBot-based chatbot depends on the specific implementation and the purpose for which you are using it. However, here are some common scenarios and examples of how the chatbot can be used:

- **Customer Support**: Provide automated support and answer frequently asked questions.
- **Information Retrieval**: Fetch and provide information on weather, news, or general knowledge.
- **Language Practice**: Engage users in language learning conversations and offer feedback.
- **Product Recommendations**: Assist users in finding relevant products based on their preferences.
- **Virtual Assistant**: Help users with tasks like reminders, scheduling, and calendar management.
- **Entertainment and Engagement**: Engage users with jokes, trivia games, and personalized recommendations.

## Configuration

The chatbot's behavior and training data can be customized through the configuration file (config.yml). You can modify the following settings:

- **name**: The name of the chatbot.
- **storage_adapter**: The storage adapter used to store conversation data. By default, it is set to chatterbot.storage.SQLStorageAdapter.
- **database_uri**: The URI for connecting to the database. By default, it uses an SQLite database file (database.db).
- **logic_adapters**: The list of logic adapters used for generating responses. You can add or modify the adapters based on your requirements.
- **training_data**: The training data used to train the chatbot. It can be a list of conversation files or a custom corpus.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request.