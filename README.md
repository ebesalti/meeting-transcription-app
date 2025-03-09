# Meeting Transcription and Form Automation App

## Overview
A desktop application for Windows that streamlines the annual employee review process by automatically transcribing manager-employee conversations in real-time, extracting relevant information, and filling in a predefined Google Form.

## Features
- Real-time audio capture and transcription
- Bilingual support (Swedish and English)
- Information extraction for form filling
- Review interface for validating extracted data
- Meeting analysis and visualization
- Google Form integration
- Privacy-focused with local processing

## Technology Stack
- **Frontend**: Python with PyQt
- **Speech Processing**: OpenAI Whisper (medium model)
- **NLP**: spaCy/NLTK with optional OpenAI GPT API
- **Database**: SQLite
- **Audio Processing**: PyAudio, FFMPEG
- **Speaker Identification**: SpeechBrain/PyAnnote
- **Visualization**: Plotly/Matplotlib

## Project Structure
```
meeting-transcription-app/
├── src/                    # Source code directory
│   ├── audio/              # Audio capture and processing
│   ├── transcription/      # Speech to text conversion
│   ├── extraction/         # Information extraction from text
│   ├── form/               # Form integration
│   ├── analysis/           # Meeting analysis and visualization
│   ├── ui/                 # User interface components
│   ├── config/             # Configuration
│   ├── database/           # Database operations
│   └── main.py             # Main application entry point
├── docs/                   # Documentation
├── tests/                  # Test cases
└── requirements.txt        # Python dependencies
```

## Setup

### Prerequisites
- Python 3.8 or higher
- FFMPEG installed on the system
- Windows OS (7/10/11)

### Installation
1. Clone the repository:
```bash
git clone https://github.com/ebesalti/meeting-transcription-app.git
cd meeting-transcription-app
```

2. Create a virtual environment and activate it:
```bash
python -m venv venv
venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Download NLTK data:
```bash
python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords')"
```

5. Configure the application by creating a `.env` file in the project root directory with your API keys (if using cloud services):
```
OPENAI_API_KEY=your_openai_api_key
GOOGLE_API_KEY=your_google_api_key
```

## Usage
1. Start the application:
```bash
python src/main.py
```

2. The main window will open, allowing you to:
   - Record or import audio
   - Transcribe conversations
   - Review extracted information
   - Submit data to Google Forms

## Development
- Run tests with `pytest tests/`
- Contributions welcome via pull requests

## License
MIT License

## Acknowledgements
- OpenAI for the Whisper speech recognition model
- PyQt team for the GUI framework