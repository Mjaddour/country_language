# AI Chat Assistant with Audio Playback

This project is an AI-powered chatbot built with **Gradio** and **OpenAI**, featuring text-based responses and optional audio playback for the assistant's messages.

## Features
- **AI-Powered Chat:** Users can chat with an AI assistant to ask questions, get responses, or perform tasks.
- **Audio Playback:** A "Play Last Response" button allows users to hear the assistant's most recent response via text-to-speech.
- **Dynamic Image Output:** The assistant can optionally provide image outputs based on the conversation context.
- **Clear Chat History:** Users can clear the chat to start a new conversation.

---

## Requirements
To run this project, you need the following:
1. **Python 3.7+**
2. **Dependencies:**
   - `gradio`
   - `openai`
   - `pydub`
   - `ffmpeg` (required for audio playback)
3. **OpenAI API Key:** For accessing OpenAI's models.
4. **ffplay:** A tool from `ffmpeg` for audio playback.

---

## Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-repo-name/chat-assistant.git
   cd chat-assistant
   ```

2. **Install Python Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Install ffmpeg:**
   - On **Linux** (Ubuntu/Debian):
     ```bash
     sudo apt install ffmpeg
     ```
   - On **Mac** (Homebrew):
     ```bash
     brew install ffmpeg
     ```
   - On **Windows**: [Download ffmpeg](https://ffmpeg.org/download.html) and add it to your system PATH.

4. **Set Up OpenAI API Key:**
   - Create an `.env` file in the project root with your API key:
     ```
     OPENAI_API_KEY=your_api_key_here
     ```

---

## Usage

1. **Run the Application:**
   ```bash
   python app.py
   ```

2. **Interact with the Chatbot:**
   - Enter a message in the textbox and press "Enter" to send.
   - The chatbot will respond with text and optional images.

3. **Play Last Response:**
   - Click the "🔊 Play Last Response" button to hear the assistant's most recent reply.

4. **Clear Chat:**
   - Click the "Clear" button to reset the conversation.

---

## File Structure

```plaintext
.
├── app.py                  # Main application file
├── requirements.txt        # Python dependencies
├── README.md               # Project documentation
└── .env                    # OpenAI API Key (not included in the repo)
```

---

## How It Works

### Key Components:
1. **Chat Functionality:**
   - Handles user inputs and generates responses using OpenAI's models.
   - Adds the assistant's responses to the conversation history.

2. **Audio Playback:**
   - Converts the assistant's text responses to audio using OpenAI's text-to-speech API.
   - Plays the audio using the `ffplay` tool.

3. **Gradio Interface:**
   - Provides an interactive user interface with a chatbot, image output, and control buttons.

### Workflow:
1. User enters a message in the chatbox.
2. The chatbot processes the message and generates a response.
3. The response is displayed, and the user can optionally play the response audio.

---

## Dependencies

### Python Libraries:
- `gradio`: Interactive UI for the chatbot.
- `openai`: For generating chat responses and text-to-speech.
- `pydub`: For processing audio playback.

### System Tools:
- `ffmpeg`: Required for audio playback with `pydub`.

---

## Future Enhancements
- Add support for saving chat history.
- Extend the assistant's capabilities with more tools (e.g., scheduling, data analysis).
- Customize the voice and audio playback options.

