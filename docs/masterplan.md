# Meeting Transcription and Form Automation App

## App Overview and Objectives

This application aims to streamline the annual employee review process by automatically transcribing manager-employee conversations in real-time, extracting relevant information, and filling in a predefined Google Form. The app will operate locally on Windows machines to ensure confidentiality of sensitive employee discussions while providing valuable insights through meeting visualizations and summaries.

### Primary Objectives:
- Capture and transcribe manager-employee conversations in real-time
- Support both Swedish and English language processing
- Extract relevant information to fill specific form fields
- Provide a simple UI for reviewing and approving extracted information
- Generate meeting summaries and visualizations
- Maintain data privacy through local processing
- Learn from user corrections to improve accuracy over time

## Target Audience
- Managers and HR professionals at Softhouse conducting employee review meetings
- Employees participating in these meetings

## Core Features and Functionality

### 1. Audio Capture and Processing
- Real-time audio capture from computer output and microphone
- Support for both live meetings (Google Meet/Teams) and locally saved audio files
- Speaker identification to differentiate between manager and employee

### 2. Transcription Engine
- Integration with OpenAI Whisper (medium model) for local transcription
- Real-time transcription of 45-minute meetings
- Bilingual support (Swedish and English)
- Timestamped transcription for reference

### 3. Information Extraction
- Natural Language Processing to identify relevant information for form fields
- Hybrid approach with options for local processing or API-based extraction
- Contextual understanding of conversation to match natural dialogue to specific form questions
- Confidence scoring for extracted information

### 4. Review Interface
- Simple, intuitive UI for reviewing transcribed content
- Suggested form responses with highlighting of source text from transcription
- Edit functionality for correcting or refining extracted information
- Learning mechanism to improve from corrections

### 5. Form Integration
- Direct submission to Google Forms via API
- Export functionality to Google Docs for manual review if needed
- Validation to ensure all required fields have appropriate data

### 6. Analysis and Visualization
- Meeting summary generation highlighting key points
- Sentiment analysis of the conversation
- Key topics identification
- Action items extraction
- Visual representations of discussion themes and sentiment trends

### 7. Privacy and Security
- Fully local operation capability for sensitive information
- Encryption of stored transcripts and extracted data
- Option to automatically delete raw audio after processing
- User authentication for accessing the application

## High-Level Technical Stack Recommendations

### Frontend
- **Python with PyQt or Tkinter**: For creating a simple desktop application UI
- **Plotly or Matplotlib**: For data visualizations
- **Alternative**: Consider Electron if a more modern UI is desired in future iterations

### Backend
- **Python**: Core application logic
- **OpenAI Whisper**: Local speech-to-text model (medium variant)
- **spaCy or NLTK**: For local NLP processing
- **OpenAI GPT API** (optional): For enhanced NLP capabilities when internet connection is available
- **Google APIs**: For form submission

### Data Storage
- **SQLite**: Lightweight database for storing transcriptions and form data locally
- **File System**: For temporary audio storage and exported documents

### Processing Components
- **PyAudio**: For audio capture
- **FFMPEG**: For audio processing
- **SpeechBrain or PyAnnote**: For speaker diarization (identifying who is speaking)

## Development Phases and Milestones

### Phase 1: Core Functionality (1-2 months)
- Audio capture from multiple sources
- Basic transcription using Whisper
- Simple UI for controlling recording and viewing transcripts
- Basic form field extraction for key information
- Google Form connection for manual data transfer

### Phase 2: Enhanced Processing (1-2 months)
- Speaker diarization implementation
- Improved NLP for more accurate information extraction
- Review interface for verifying and correcting extracted data
- Direct API submission to Google Forms
- Export functionality to Google Docs

### Phase 3: Analysis and Refinement (1-2 months)
- Meeting summary generation
- Basic sentiment analysis and topic modeling
- Visualization dashboard
- Learning from user corrections
- Testing and optimization for performance

### Phase 4: Polish and Additional Features (1 month)
- UI refinements based on user feedback
- Enhanced visualization options
- Additional language support refinements
- Documentation and user guides
- Deployment packaging for easy installation