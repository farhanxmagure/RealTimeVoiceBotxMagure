# RealTimeVoiceBotxMagure

## Overview
RealTimeVoiceBotxMagure is an advanced AI-driven voice assistant built using Python, OpenAI's Realtime API, Chainlit, and WebSockets. It provides real-time conversational support, handling both text and voice inputs. The bot is designed to offer seamless interaction for customer service applications, particularly for an online store called "ShopMe."

## Features
- **Real-Time Voice and Text Interaction**: Users can communicate with the bot using either voice or text.
- **OpenAI Realtime API Integration**: Handles natural language understanding and response generation.
- **WebSockets for Low-Latency Communication**: Ensures quick and smooth interaction.
- **Asynchronous Processing**: Uses `asyncio` to efficiently manage concurrent tasks.
- **Custom Tool Integration**: Expands chatbot capabilities with external API interactions.
- **User Session Management**: Maintains conversation context and user tracking.
- **Error Handling and Logging**: Logs errors for debugging and monitoring.

## Screenshot
![Application Screenshot](https://github.com/farhanxmagure/RealTimeVoiceBotxMagure/blob/main/Screenshot%202025-02-12%20160921.png)

## Installation
### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- Virtual environment (optional but recommended)
- Dependencies listed in `requirements.txt`

### Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/farhanxmagure/RealTimeVoiceBotxMagure.git
   cd RealTimeVoiceBotxMagure
   ```
2. Create a virtual environment (optional but recommended):
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Set up environment variables:
   ```sh
   export AZURE_OPENAI_API_KEY='your_api_key'
   export AZURE_OPENAI_ENDPOINT='your_endpoint_url'
   export AZURE_OPENAI_DEPLOYMENT='your_deployment_name'
   ```
   On Windows (Command Prompt):
   ```sh
   set AZURE_OPENAI_API_KEY=your_api_key
   set AZURE_OPENAI_ENDPOINT=your_endpoint_url
   set AZURE_OPENAI_DEPLOYMENT=your_deployment_name
   ```
5. Run the application:
   ```sh
   python app.py
   ```

## Project Structure
```
RealTimeVoiceBotxMagure/
│-- app.py           # Main chatbot application logic
│-- __init__.py      # Handles real-time API connection
│-- tools.py         # Defines chatbot skills
│-- requirements.txt # Dependencies
│-- README.md        # Project documentation
```

## How It Works
1. **User Interaction**: The bot accepts text and voice input.
2. **Processing**:
   - `app.py` sends user input to the OpenAI Realtime API.
   - `__init__.py` manages the WebSocket connection and event handling.
   - `tools.py` provides additional chatbot functionalities (e.g., checking order status).
3. **Response Generation**:
   - OpenAI generates a response and returns it.
   - If needed, the bot invokes tools to retrieve external data.
4. **User Feedback**: The chatbot displays responses in text or plays generated audio.

## Key Technologies
- **Python**: Core programming language
- **AsyncAzureOpenAI**: Handles OpenAI API requests asynchronously
- **Chainlit**: Simplifies chatbot UI and interaction
- **WebSockets**: Enables real-time communication
- **UUID**: Manages unique user sessions
- **Logging**: Captures errors and events
