# Gemini Flight Booking Agent ✈️

An intelligent, tool-augmented chatbot built with the Gemini 1.5 Flash API. This agent can check ticket prices, book flights, and retrieve booking details directly from a local SQLite database using function calling.

## 🌟 Key Features
- **Function Calling (Tool Use):** The agent autonomously decides when to query the database or book a flight based on user intent.
- **Database Integration:** Persistent storage using SQLite (`flight_booking.db`) to manage ticket prices and passenger bookings.
- **Interactive UI:** A clean web interface built with **Gradio** for real-time chatting.
- **Modular Design:** Notebook-based architecture using `%run` for clean separation of concerns (tools, database, config, and UI).

## 📁 Project Structure
- **`main.ipynb`**: The entry point. It initializes the Gradio interface and manages the chat loop.
- **`tools_fun.ipynb`**: Contains the Python logic for database operations (Get/Set Price, Book Flight, Get Details).
- **`tools_handle.ipynb`**: The "brain" that processes Gemini's tool call requests and maps them to Python functions.
- **`db_config.ipynb`**: Handles the SQLite schema creation and connection setup.
- **`config.ipynb`**: Manages environment variables and Gemini API client initialization.
- **`imports.ipynb`**: Centralized location for all required libraries (OpenAI SDK, Gradio, dotenv).

## 🛠️ Setup Instructions

### 1. Prerequisites
- Python 3.10+
- A Google Gemini API Key

### 2. Environment Configuration
Create a `.env` file in the root directory and add your API key:
```env
GOOGLE_API_KEY=your_gemini_api_key_here