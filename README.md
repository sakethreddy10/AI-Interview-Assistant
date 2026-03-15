# AI Interview Assistant

An intelligent interview assistant that conducts natural, conversational interviews using AI. The system features voice recording, real-time transcription, and adaptive questioning based on candidate responses.

## Features

- **Conversational AI Interviewer**: Conducts natural interviews with adaptive questioning
- **Voice Recording & Transcription**: Records audio responses and transcribes them using AssemblyAI
- **Text-to-Speech**: Generates audio feedback using Murf AI
- **Real-time Chat Interface**: Modern web interface with live conversation
- **Subject-Specific Interviews**: Supports interviews for different subjects
- **Memory Checkpointing**: Maintains conversation context using LangGraph

## Tech Stack

### Backend
- **Flask**: Web framework
- **LangChain**: AI orchestration and agent creation
- **LangGraph**: Conversation flow management
- **AssemblyAI**: Speech-to-text transcription
- **Murf AI**: Text-to-speech generation
- **Google Gemini**: AI model for interview logic

### Frontend
- **HTML/CSS/JavaScript**: Core web technologies
- **Tailwind CSS**: Styling framework
- **Font Awesome**: Icons
- **Web Audio API**: Audio recording

## Prerequisites

- Python 3.8+
- Node.js (for frontend development, optional)
- API Keys for:
  - Google AI (Gemini)
  - AssemblyAI
  - Murf AI

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/sakethreddy10/AI-Interview-Assistant.git
   cd AI-Interview-Assistant
   ```

2. **Backend Setup**
   ```bash
   cd backend
   pip install -r requirements.txt
   ```

3. **Environment Variables**
   
   Create a `.env` file in the `backend/` directory with the following variables:
   ```
   GOOGLE_API_KEY=your_google_api_key
   MURF_API_KEY=your_murf_api_key
   ASSEMBLYAI_API_KEY=your_assemblyai_api_key
   ```

4. **Frontend Setup**
   
   The frontend is static HTML/CSS/JS, so no additional setup is required. Simply open `frontend/index.html` in a browser or serve it via a web server.

## Running the Application

1. **Start the Backend**
   ```bash
   cd backend
   python app.py
   ```
   The backend will run on `http://localhost:5000`

2. **Open the Frontend**
   
   Open `frontend/index.html` in your web browser, or serve the `frontend/` directory using a local web server.

## Usage

1. Select an interview subject from the available options
2. Click "Start Interview" to begin
3. The AI interviewer will ask questions - respond verbally or via text
4. Use the record button to capture audio responses
5. The system will transcribe your speech and continue the conversation
6. Complete all 5 questions for a full interview session

## API Endpoints

- `POST /start_interview`: Initialize a new interview session
- `POST /ask_question`: Get the next interview question
- `POST /transcribe`: Transcribe audio data
- `POST /generate_audio`: Generate TTS audio from text

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.