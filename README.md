# ChatBot

This is a simple chatbot implementation using the ChatterBot library in Python. The chatbot is designed to engage in conversations with users, providing pre-defined responses based on the training data.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Configuration](#configuration)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Installation

1. Clone or Download the repository to your local machine using the following command:
```
git clone https://github.com/kershrita/ChatBot.git
```
2. Install the necessary libraries.
```
pip install nltk chatterbot spacy
```
```
pip install --upgrade sqlalchemy
```
3. Take [sql_storage.py](sql_storage.py) file to this path.
```
[system path]\anaconda3\Lib\site-packages\chatterbot\storage
```

## Usage

1. Open the notebook, you can find two separate code. One's for the customized training and the other to train using ready corpus data.
2. Feel free to post in issues if there is a problem.
3. You can watch this for more description [tutorial video](https://www.youtube.com/watch?v=qextOtQr1Ac)

## Features

- **Natural Language Processing**: The chatbot utilizes natural language processing techniques to understand user input and generate appropriate responses.
- **Pre-trained Models**: The chatbot comes with pre-trained language models that provide a starting point for conversations.
- **Ready Corpus**: It's also comes with a different language corpus data, you can find it [here](https://github.com/gunthercox/chatterbot-corpus).
- **Customizable Training**: You can train the chatbot with your own conversational data to make it more specific to your use case.
- **Multiple Logic Adapters**: The chatbot supports multiple logic adapters that handle different aspects of conversation generation, such as mathematical calculations, sentiment analysis, or fallback responses.
- **Storage Adapter**: The chatbot uses a storage adapter to persist conversation data, allowing you to resume conversations and track user interactions.

## Configuration

The chatbot's behavior and training data can be customized:

- **Customer Support**: Provide automated support and answer frequently asked questions.
- **Information Retrieval**: Fetch and provide information on weather, news, or general knowledge.
- **Language Practice**: Engage users in language learning conversations and offer feedback.
- **Product Recommendations**: Assist users in finding relevant products based on their preferences.
- **Virtual Assistant**: Help users with tasks like reminders, scheduling, and calendar management.
- **Entertainment and Engagement**: Engage users with jokes, trivia games, and personalized recommendations.

## Documentation

- **[ChatterBot](https://chatterbot.readthedocs.io/en/stable/index.html)**: is a Python library that enables developers to create chatbots with natural language processing capabilities. It provides a simple and flexible framework for building conversational agents that can engage in interactive conversations.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request.


## License

Chatbot is released under the [MIT License](LICENSE).

## Contact

- Mail: ashrafabdulkhaliq80@gmail.com
- LinkedIn: https://www.linkedin.com/in/ashraf-abdulkhaliq
- GitHub: https://github.com/kershrita