# Python AI Assistant 🤖

A conversational CLI chatbot powered by OpenRouter API and LLMs, built using the OpenAI Python SDK. The assistant maintains conversation history to provide context-aware, interactive dialogues directly in the terminal.

---

### 📌 Features

* **OpenRouter & OpenAI SDK Integration:** Seamlessly interacts with the `openrouter/auto` model via the `openai` Python library.
* **Contextual Memory:** Keeps track of the chat history across the session for continuous, context-aware conversations.
* **Secure Environment Configuration:** Utilizes `python-dotenv` to safely load API keys from local environment variables.
* **Interactive CLI Interface:** Clean terminal loop with exit commands (`exit` or `quit`) to terminate sessions gracefully.

---

### 🛠️ Prerequisites

* Python 3.8 or higher
* An OpenRouter API key (obtainable at [openrouter.ai](https://openrouter.ai))

---

### 🚀 Getting Started

**1. Clone the repository**
```bash
git clone [https://github.com/AybenizEsgerkhanova/python-ai-assistant.git](https://github.com/AybenizEsgerkhanova/python-ai-assistant.git)
cd python-ai-assistant 
```
2. Set up a virtual environment (Recommended)

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

3. Install dependencies

```bash
pip install openai python-dotenv
```
4. Configure environment variables
Create a .env file in the root directory:

Kod hissəsi
OPENRouter_API_KEY=your_openrouter_api_key_here
⚠️ Security Note: Never commit your .env file to version control. Ensure .env is listed inside your .gitignore.


💻 Usage
Run the project directly via Jupyter Notebook (.ipynb) or execute the Python script:

Python
import os
from openai import OpenAI
from dotenv import load_dotenv

load_dotenv()

client = OpenAI(
    api_key=os.getenv("OPENRouter_API_KEY"),
    base_url="[https://openrouter.ai/api/v1](https://openrouter.ai/api/v1)"
)

# Start the interactive assistant
start_chat(client)
Type your prompt to converse, and type exit or quit to end the session.

📄 License
This project is open source and available under the MIT License.
