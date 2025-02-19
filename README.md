# Enhanced NLP Chatbot

## Overview

The **Enhanced NLP Chatbot** is a Python-based conversational assistant that leverages Natural Language Processing (NLP) and a deep learning model built with TensorFlow and NLTK. It features a user-friendly graphical interface developed with Tkinter. The chatbot can respond to user queries, perform web searches, provide the current time, and more.

## Features

- **Interactive GUI**: Built using Tkinter for a simple and intuitive user experience.
- **Deep Learning Powered**: Utilizes a TensorFlow model to generate responses based on user input.
- **NLP Capabilities**: Uses NLTK for text tokenization and lemmatization.
- **Special Commands**:
  - Type `exit`, `quit`, or `bye` to end the conversation.
  - Type `search <query>` to open a web search in your default browser.
  - Type `time` to display the current time.
- **Chat Management**:
  - **Clear Chat**: Clears the conversation history.
  - **Save Chat**: Saves the conversation history to a text file.
  - **Help**: Displays usage instructions.

## Prerequisites

- Python 3.10 or later
- The following Python packages:
  - `tkinter` (usually included with Python on Windows)
  - `numpy`
  - `nltk`
  - `tensorflow`
  - Other built-in libraries: `json`, `pickle`, `random`, `webbrowser`, `datetime`

## Installation

### 1. Clone the Repository

Open your terminal or command prompt and run:

```bash
git clone https://github.com/Shivanipandey29/Nlp_Chatbot.git
cd Nlp_Chatbot
2. (Optional) Create a Virtual Environment
It's a good idea to work within a virtual environment:

bash

python -m venv venv
Activate the virtual environment:

Windows:
source venv/bin/activate
3. Install Required Packages
If you have a requirements.txt file, install using:

bash
pip install -r requirements.txt
Otherwise, install packages manually:

bash

pip install numpy nltk tensorflow
4. Download NLTK Data
Open a Python shell and run:

python

import nltk
nltk.download('punkt')
nltk.download('wordnet')
File Structure

graphql
Nlp_Chatbot/
├── Data/
│   ├── intents.json          # Contains intents, patterns, and responses for the chatbot.
│   ├── chatbot_model.h5      # Trained TensorFlow model (generated after training).
│   ├── words.pkl             # Pickle file containing tokenized words.
│   ├── classes.pkl           # Pickle file containing intent classes.
│   ├── gui.py                # Tkinter GUI for the chatbot.
│   └── main.py               # Model training script.
├── README.md                 # This file.
└── requirements.txt          # (Optional) List of required Python packages.

Usage
1. Train the Model
Before running the chatbot, you need to train the model. This step processes the intents and generates the necessary model and pickle files.

Run the training script:

python main.py
When the training completes, you should see a message like Done, and the files chatbot_model.h5, words.pkl, and classes.pkl will be created in the appropriate directory.

2. Run the Chatbot GUI
Once the model is trained, run the chatbot interface:

python gui.py
A window will open with the chat interface. Type your message and press Enter or click the Send button to interact with the chatbot.

Customization
Intents: Edit the Data/intents.json file to modify or add new intents, patterns, and responses.
GUI: The GUI code in Data/gui.py can be customized to change the look and feel of the application.
Training Parameters: Modify main.py to adjust training parameters (e.g., number of epochs, batch size).
Troubleshooting
Missing Modules: Ensure all required Python packages are installed.
NLTK Data Issues: Confirm that punkt and wordnet are downloaded via NLTK.
Model Not Found: If chatbot_model.h5 is missing, re-run the training script.

License
This project is licensed under the MIT License.

Acknowledgments
Built using Python, TensorFlow, NLTK, and Tkinter.
Inspired by various open-source chatbot projects.
