Intents-Based Chatbot Using NLP and Logistic Regression

This project implements a chatbot that utilizes Natural Language Processing (NLP) techniques and Logistic Regression to understand and respond to user inputs based on predefined intents. The chatbot is built using Python and hosted on a Streamlit web interface, allowing users to interact with the bot seamlessly.


---

Features

1. Intents-Based Classification:
The chatbot identifies the user's intent from predefined patterns and provides appropriate responses.


2. Interactive Interface:
A user-friendly interface is built using the Streamlit framework for real-time interaction.


3. Conversation History:
User and chatbot interactions are logged in a CSV file for later reference.


4. Customizable Intents:
Intents are stored in a JSON file, making it easy to add or modify intents and patterns.




---

Prerequisites

Python 3.7 or above

Internet connection (for downloading NLTK data)



---

Installation

1. Clone the Repository:

git clone https://github.com/your-username/chatbot.git
cd chatbot


2. Install Dependencies:
Install the required Python libraries using the following command:

pip install -r requirements.txt


3. Prepare NLTK Data:
Ensure NLTK data is available:

import nltk
nltk.download('punkt')


4. Run the Application:
Launch the Streamlit app:

streamlit run app.py




---

Project Structure

chatbot/
├── app.py                   # Main application file
├── intents.json             # JSON file containing intents and patterns
├── requirements.txt         # List of Python dependencies
├── chat_log.csv             # Conversation history (generated after first use)
├── nltk_data/               # Folder for NLTK data (optional)
└── README.md                # Project documentation


---

Usage

1. Launch the chatbot using the Streamlit interface.


2. Type your message in the input box, and the chatbot will respond based on its trained intents.


3. Navigate to the "Conversation History" tab to view past interactions.


4. Modify intents.json to add or update intents and patterns.




---

Intents JSON Structure

The intents.json file contains a list of intents, each with the following structure:

[
    {
        "tag": "greeting",
        "patterns": ["Hi", "Hello", "Hey there"],
        "responses": ["Hello!", "Hi there!", "Greetings!"]
    },
    {
        "tag": "goodbye",
        "patterns": ["Bye", "Goodbye", "See you later"],
        "responses": ["Goodbye!", "See you soon!", "Take care!"]
    }
]

tag: A unique identifier for the intent.

patterns: A list of possible user inputs that correspond to the intent.

responses: A list of potential responses the chatbot can use for the intent.



---

How It Works

1. Text Preprocessing:
The user input is tokenized and transformed using TF-IDF vectorization.


2. Model Training:
Logistic Regression is trained on the patterns from the intents.json file.


3. Prediction:
The model predicts the intent of the user input and selects a random response from the corresponding intent.


4. Logging:
All interactions are logged in chat_log.csv with timestamps.




---

Future Enhancements

1. Integrate advanced NLP techniques like BERT or GPT models for improved accuracy.


2. Add support for multilingual intents and responses.


3. Incorporate a database for storing intents and conversation history.


4. Enhance the UI with richer design elements.




---

License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it.


---

Contribution

Contributions are welcome! To contribute:

1. Fork the repository.


2. Create a feature branch: git checkout -b feature-name.


3. Commit your changes: git commit -m 'Add feature-name'.


4. Push to the branch: git push origin feature-name.


5. Open a pull request.




---

Acknowledgments

This project utilizes the following libraries and frameworks:

NLTK

scikit-learn

Streamlit



---

Contact

For any queries or feedback, feel free to reach out at anirudh.mamilla1@gmail.com
