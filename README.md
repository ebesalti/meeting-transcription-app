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
- **Frontend**: Python with PyQt/Tkinter
- **Speech Processing**: OpenAI Whisper (medium model)
- **NLP**: spaCy/NLTK with optional OpenAI GPT API
- **Database**: SQLite
- **Audio Processing**: PyAudio, FFMPEG
- **Speaker Identification**: SpeechBrain/PyAnnote
- **Visualization**: Plotly/Matplotlib

## Setup
See the docs/installation.md file for detailed setup instructions.

## Usage
See the docs/usage.md file for detailed usage instructions.

## Development
See the docs/development.md file for development guidelines.

## License
MIT License