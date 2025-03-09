
# MeetingWisdom

MeetingWisdom is a modern web application that provides real-time meeting transcription and summarization with actionable insights. It uses the browser’s SpeechRecognition (Google Web Speech API) for live transcription and directly calls the OpenAI API to generate summaries. The application is designed with a responsive, modern UI using Bootstrap and includes settings for API key, system prompt, language, and GPT model selection. All user inputs are persisted in local storage for convenience.

## Features

- **Real-Time Transcription:**  
  Uses the Google Web Speech API for continuous speech recognition with support for multiple languages (e.g., English (US), English (India), Japanese).

- **Real-Time Summarization:**  
  Calls the OpenAI API (with selectable GPT models) to generate a summary of the transcription, providing meeting insights.

- **Customizable Settings:**  
  Configure your OpenAI API key, system prompt, language for transcription, and select your preferred GPT model. These settings are managed via a collapsible Bootstrap accordion.

- **Responsive UI:**  
  The transcription and summary sections are displayed side-by-side and are scrollable for better usability on different devices.

- **MIT Licensed:**  
  This project is released under the MIT License.

## Demo

[Demo video on YouTube](https://youtu.be/6sklv4R_r6o)

## Setup

### Prerequisites

- A modern web browser (Google Chrome is recommended for SpeechRecognition support).
- An OpenAI API key.  
  See the [Help section](#help-how-to-get-your-openai-api-key) below for instructions.

### Running Locally

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/MasayukiTanaka0412/MeetingWisdom.git
   cd meetingwisdom
   ```

2. **Serve the Application:**

   Since MeetingWisdom is a static HTML/JavaScript application, you can serve it using any web server. For example, with Python:

   ```bash
   # Python 3.x
   python -m http.server 8000
   ```

   Then, open your browser and navigate to [http://localhost:8000](http://localhost:8000).

3. **Using the Application:**

   - Click the accordion header to open the **Settings** panel.
   - Enter your OpenAI API key and click "Set API Key".
   - Optionally, enter a custom system prompt (multiline) and click "Set Prompt".
   - Select your preferred language and GPT model, then click the corresponding "Set" button.
   - Start transcription by clicking the **Start Transcription** button.
   - When you finish speaking, click **Stop Transcription**.
   - Click **Summarize** to generate and display the meeting summary.

## Configuration

- **API Key:**  
  Your API key is saved in your browser’s local storage for convenience. For production use, ensure you protect your API key by proxying requests through a secure backend.

- **System Prompt:**  
  Customize the system prompt that guides the summarization. This prompt is also stored in local storage.

- **Language:**  
  Choose the language for transcription from the dropdown (e.g., `en-US`, `en-IN`, `ja-JP`).

- **GPT Model Selection:**  
  The available models include:  
  - gpt-4o-mini  
  - gpt-4o
  - gpt-4.5-preview

  The selected model is used for generating summaries.

## License

MeetingWisdom is released under the MIT License.

---

## Help: How to Get Your OpenAI API Key

To use the OpenAI API, you'll need an API key. Follow these steps:

1. **Sign Up / Log In:**  
   Visit the [OpenAI Platform](https://platform.openai.com/signup) and create an account or log in.

2. **Access Your Dashboard:**  
   Once logged in, navigate to your account dashboard.

3. **Create a New API Key:**  
   In the API keys section, click “Create new secret key” to generate a new key.

4. **Copy and Save:**  
   Copy the generated API key and keep it safe. Paste it into the "OpenAI API Key" input in MeetingWisdom.

5. **Security Reminder:**  
   Do not share your API key publicly. For production, use a secure backend to proxy your API calls.

Your API key will be stored in your browser's local storage for convenience.

---

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests for improvements or new features.

## Contact

For any questions or suggestions, please open an issue in the repository or contact the maintainer at masayuki.tanaka.0412@gmail.com

