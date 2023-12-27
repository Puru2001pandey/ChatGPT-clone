# 💬 ChatGPT Full-Stack Clone

A full-stack replica of the ChatGPT interface. It features a modern, dark-mode UI inspired by OpenAI, integrates the OpenAI API to generate real-time conversational responses, and persists chat sessions in a MongoDB database.


## ✨ Features

- **Conversational AI**: Integrates the OpenAI API (`text-davinci-003`) to process questions and provide real-time responses.
- **Database Persistence**: Connected to MongoDB Atlas via PyMongo to save chat history and reload past conversations on page refresh.
- **Sleek UI/UX**: Recreated the modern ChatGPT dark-mode chat interface, utilizing Tailwind CSS for custom styling and responsiveness.
- **Dynamic Sidebar**: A sidebar list displaying active chat threads stored in the database.
- **Lightweight Backend**: Built on a Flask micro-framework handling server routes, database requests, and OpenAI API calls.

## 🛠️ Tech Stack

* **Frontend**: HTML5, CSS3, JavaScript, Tailwind CSS (utility-first styling).
* **Backend**: Python, Flask (routing and server API).
* **Database**: MongoDB Atlas (noSQL storage for chat data).
* **API Integration**: OpenAI Python Client.

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- MongoDB Database (Local or Atlas cloud instance)
- OpenAI API Key

### Installation & Local Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Puru2001pandey/ChatGPT-clone.git
   cd ChatGPT-clone
   ```

2. **Create a virtual environment & install dependencies:**
   ```bash
   python -m venv venv
   # Activate on Windows
   venv\Scripts\activate
   # Activate on macOS/Linux
   source venv/bin/activate

   pip install flask flask_pymongo openai
   ```

3. **Configure Environment Variables:**
   Update your database URI and OpenAI API credentials inside `main.py` to point to your respective configurations.

4. **Start the Flask server:**
   ```bash
   python main.py
   ```
   The application will run on `http://127.0.0.1:5001`.

## 💡 How It Works

1. **User input**: The user types a message in the browser text bar and clicks send.
2. **API route**: A POST request containing the prompt is sent to the `/api` endpoint.
3. **OpenAI & MongoDB**: Flask queries MongoDB to check if the question has already been answered. If not, it requests a new response from the OpenAI API, stores it in MongoDB, and returns it.
4. **DOM Update**: The response is rendered dynamically in the chat window.

## 📜 License

Distributed under the MIT License. See `LICENSE` for details.
