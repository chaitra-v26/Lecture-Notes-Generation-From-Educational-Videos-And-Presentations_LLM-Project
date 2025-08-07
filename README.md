# 🎓 Lecture Notes Generation from Educational Videos and Presentations

> **Advanced Speech-to-Text and AI-Powered Educational Content Transformation System**

**Technologies**: Python 3.8+ | Gradio Web Interface | Google Gemini AI | OpenAI Whisper

## 📋 Overview

This project is an **intelligent educational content processing system** that automatically converts lecture videos and presentation slides into structured, comprehensive study materials. Developed as part of the Large Language Models & Their Applications hackathon, it combines advanced speech-to-text technology with AI-powered content generation to create high-quality lecture notes, quiz questions, and conceptual diagrams.

### 🌟 Key Features

- **🎥 Video Transcription**: Extract audio from MP4 lecture videos and convert speech to text using OpenAI Whisper
- **📄 Multi-format Slide Processing**: Extract text content from PDF, PPT, and PPTX presentation files
- **🤖 AI-Powered Note Generation**: Transform raw content into well-structured Markdown lecture notes using Google Gemini 1.5 Pro
- **❓ Automated Quiz Creation**: Generate relevant questions and answers for self-assessment
- **📊 Conceptual Diagrams**: Create ASCII-style visual representations of key concepts
- **📈 Quality Evaluation**: Automated scoring system based on educational quality metrics
- **🌐 Interactive Web Interface**: User-friendly Gradio-based GUI for seamless interaction

## 🏗️ Project Architecture

```
Lecture-Notes-Generation/
├── CODE BASE/
│   └── 044_045_046_900.ipynb      # Main Jupyter notebook with all functionality
├── OUTPUTS/
│   ├── lecture_transcript.txt      # Extracted audio transcription
│   ├── slides_text.txt            # Combined slide content
│   ├── input.txt                  # Merged transcript + slides
│   ├── lecture_notes.md           # AI-generated structured notes
│   ├── lecture_questions.md       # Auto-generated quiz questions
│   ├── diagrams.md               # Conceptual ASCII diagrams
│   └── evaluation_report.md       # Quality assessment report
├── generate_notes_gradio.py       # Gradio web interface (optional)
├── evaluate_notes.py             # Evaluation system (optional)
├── README.md                     # Project documentation
└── requirements.txt              # Python dependencies
```

## 🛠️ Tech Stack

### Core Technologies
- **Python 3.8+** - Primary programming language
- **Google Gemini 1.5 Pro** - Large Language Model for content generation
- **OpenAI Whisper** - Advanced speech-to-text transcription
- **Gradio** - Interactive web interface framework

### Libraries & Dependencies
- **Audio/Video Processing**:
  - `moviepy` - Video-to-audio conversion
  - `whisper` - Speech recognition and transcription
  
- **Document Processing**:
  - `python-pptx` - PowerPoint file processing
  - `pdfminer.six` - PDF text extraction
  - `PyMuPDF` - Alternative PDF processing
  
- **AI & ML**:
  - `google-generativeai` - Google Gemini API integration
  
- **Web Interface**:
  - `gradio` - Interactive web application framework
  
- **Utilities**:
  - `regex` - Pattern matching for evaluation scoring
  - `markdown` - Text formatting and structure

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/Lecture-Notes-Generation-From-Educational-Videos-And-Presentations_LLM-Project.git
cd Lecture-Notes-Generation-From-Educational-Videos-And-Presentations_LLM-Project
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

**Manual Installation (if requirements.txt is unavailable):**
```bash
pip install gradio google-generativeai openai-whisper moviepy python-pptx pdfminer.six PyMuPDF regex markdown
```

### 3. Configure API Keys
Obtain a Google Gemini API key from [Google AI Studio](https://makersuite.google.com/app) and configure it in your environment:

```python
import google.generativeai as genai
genai.configure(api_key="YOUR_GEMINI_API_KEY_HERE")
```

### 4. Set Up Directory Structure
```bash
mkdir OUTPUTS
mkdir Uploads
```

## 🚀 Usage Guide

### Method 1: Jupyter Notebook (Recommended)
1. **Open the main notebook**: `CODE BASE/044_045_046_900.ipynb`
2. **Upload your files** when prompted:
   - Lecture video (MP4 format)
   - Presentation slides (PDF, PPT, PPTX)
3. **Run all cells** to execute the complete pipeline
4. **Check the OUTPUTS folder** for generated materials

### Method 2: Gradio Web Interface
```bash
python generate_notes_gradio.py
```
1. Open the provided local URL in your browser
2. Paste or upload your lecture content
3. Click "Generate Notes, Q&A & Diagrams"
4. View and download the generated materials

### Method 3: Command Line Processing
```bash
# Generate notes
python generate_notes.py

# Evaluate quality
python evaluate_notes.py
```

## 📊 Output Files Description

| File | Description | Content |
|------|-------------|---------|
| `lecture_transcript.txt` | Raw audio transcription | Speech-to-text output from video |
| `slides_text.txt` | Extracted slide content | Combined text from all presentation files |
| `input.txt` | Combined input | Merged transcript and slide content |
| `lecture_notes.md` | **Main Output** | Structured, formatted lecture notes with emojis and styling |
| `lecture_questions.md` | Quiz materials | 5-10 Q&A pairs for self-assessment |
| `diagrams.md` | Visual concepts | ASCII-style conceptual diagrams |
| `evaluation_report.md` | Quality assessment | Automated scoring based on 5 educational criteria |

## 🎯 Key Features Breakdown

### 1. Multi-Modal Content Extraction
- **Video Processing**: Converts MP4 files to audio, then uses Whisper for accurate transcription
- **Document Processing**: Handles PDF, PPT, and PPTX files with fallback mechanisms
- **Smart Combination**: Merges all content with clear section headers

### 2. AI-Powered Content Generation
- **Structured Notes**: Creates well-organized content with headings, bullet points, and examples
- **Enhanced Formatting**: Adds emojis, styling, and visual hierarchy for better readability
- **Quiz Generation**: Produces relevant questions in Q&A format for learning reinforcement

### 3. Quality Assurance
- **Automated Evaluation**: Scores based on Accuracy, Completeness, Organization, Readability, and Value-Added
- **Percentage Scoring**: Provides quantitative assessment (Target: 70%+ accuracy)
- **Detailed Feedback**: Explains scoring rationale for each criterion

## 📈 Performance Metrics

Based on testing and evaluation:
- **Accuracy**: 72% (as reported in hackathon evaluation)
- **Processing Time**: ~2-5 minutes per lecture (depending on length)
- **Supported Formats**: MP4, PDF, PPT, PPTX
- **Content Quality**: Structured, comprehensive, and study-ready

## 👥 Team Contributors

**Team Members:**
- C Hemachandra (PES1UG22AM044)
- Chaitra V (PES1UG22AM045)  
- Chandana B S (PES1UG22AM046)
- Arpitha Venugopal (PES1UG22AM900)

## 🔮 Future Enhancements

- [ ] **PDF Export**: Convert generated notes to PDF format
- [ ] **Multi-language Support**: Transcription and generation in multiple languages
- [ ] **Real-time Processing**: Live lecture note generation during ongoing classes
- [ ] **Integration APIs**: Connect with Learning Management Systems (LMS)
- [ ] **Advanced Diagrams**: Generate flowcharts and mind maps
- [ ] **Collaborative Features**: Multi-user editing and sharing capabilities

## 🐛 Troubleshooting

### Common Issues:
1. **API Key Errors**: Ensure your Gemini API key is valid and properly configured
2. **File Upload Issues**: Check file formats (supported: MP4, PDF, PPT, PPTX)
3. **Memory Errors**: For large files, consider processing in smaller chunks
4. **Network Issues**: Stable internet required for API calls to Gemini

### Performance Tips:
- Use high-quality audio for better transcription accuracy
- Ensure slide text is clear and readable for better extraction
- Process one lecture at a time for optimal performance

## 🙏 Acknowledgements

- **Google Generative AI** for providing the Gemini 1.5 Pro model
- **OpenAI** for the Whisper speech-to-text technology
- **Gradio Team** for the intuitive web interface framework
- **PES University** for hosting the LLM Applications Hackathon
- **All open-source contributors** whose libraries made this project possible

---

**📧 Contact**: For questions or contributions, please reach out to any of the team members listed above.

**⭐ Star this repository** if you find it helpful for your educational content processing needs!
