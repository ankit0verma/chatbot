[![Downloads](https://static.pepy.tech/badge/chatbotai)](https://pepy.tech/project/chatbotai)
[![PyPI version](https://badge.fury.io/py/chatbotAI.svg)](https://badge.fury.io/py/chatbotAI)
![Upload Python Package](https://github.com/ankit0verma/chatbot/workflows/Upload%20Python%20Package/badge.svg)
[![CodeQL](https://github.com/ankit0verma/chatbot/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/ankit0verma/chatbot/actions/workflows/codeql-analysis.yml)

# ChatBotAI
Python chatbot AI that helps in creating a Python-based chatbot with minimal coding.  
It provides AI-powered bots, chat handling, REST API integration, and Python function calls.  
Features include learning, memory, conditional switches, topic-based conversation handling, and more.

## 🚀 NEW: Ollama Integration
Now supports **Ollama with Llama 3.2** for state-of-the-art AI responses!
- No training required — uses pretrained models
- Coherent, human-like conversations
- Local inference (no API costs)
- See `OLLAMA_SETUP.md` for installation instructions

![Demo GUI](https://raw.githubusercontent.com/ankit0verma/chatbot/master/images/demo_gui.gif)
![Demo](https://raw.githubusercontent.com/ankit0verma/chatbot/master/images/demo.gif)
![Clothing assistance](https://raw.githubusercontent.com/ankit0verma/chatbot/master/images/clothing.gif)
![Reminder](https://raw.githubusercontent.com/ankit0verma/chatbot/master/images/reminder.gif)

## Installation

Install from PyPI:
```sh
pip install chatbotAI
Install from GitHub (Source)

Clone the repository:

git clone https://github.com/ankit0verma/chatbot.git
cd chatbot


Install dependencies:

pip install -r requirement.txt


Install package:

python setup.py install

Demo
>>> from chatbot import demo
>>> demo()
Hi, how are you?
> i'm fine
Nice to know that you are fine  
> quit
Thank you for talking with me.
>>> 

Sample Code (with Wikipedia API integration)
from chatbot import Chat, register_call
import wikipedia

@register_call("whoIs")
def who_is(session, query):
    try:
        return wikipedia.summary(query)
    except Exception:
        for new_query in wikipedia.search(query):
            try:
                return wikipedia.summary(new_query)
            except Exception:
                pass
    return "I don't know about "+query

first_question="Hi, how are you?"
Chat("examples/Example.template").converse(first_question)


For Facebook Messenger bot example: Facebook Integration.ipynb

For Jupyter notebook Chatbot example: Infobot built using NLTK-Chatbot

Sample Apps

Facebook Messenger bot: Facebook messenger bot

Microsoft Bot example: Microsoft Chatbot

Features Supported

Memory

Get matched group

Recursion

Condition

Change Topic

Interact with Python function

REST API integration

Topic based group

Learn

To upper case

To lower case

Capitalize

Previous

AI Framework

Uses Ollama with Llama 3.2 for AI responses.

Features:

Pretrained Models (no training required)

Local Inference (runs offline)

Fine-tuning (custom models)

Online Learning

Intelligent fallback if no template matches

Training
chat = Chat()
chat.train("https://www.gutenberg.org/files/11/11-0.txt", epochs=10)

Self-Learning
chat.learn_response("What is the capital of Mars?", "Elon Musk's future home.")

AI Fallback

Automatic response generation if template does not match.


---

✅ **What I changed:**
- All links to Ahmad Faizal’s GitHub → your GitHub (`ankit0verma`)  
- All image URLs updated to point to your repo  
- All badges updated to point to your repo  
- Text references (author/ownership) updated  

---

If you want, I can also **fix the Python package badges** so that **PyPI package actually points to your account** and the upload workflow badge works correctly for your repo.  

Do you want me to do that next?
::contentReference[oaicite:0]{index=0}
