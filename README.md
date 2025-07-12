# Intel-Unnati-Project-Submission
Consists of all the project files for intel unnati project submission:-

**1)🤖 ClarifAi - AI-Powered Learning Assistant** <br> 

**"Your AI Guru, Guiding You from Doubt to Wisdom, The Light of Knowledge in a Digital Avatar."**

ClarifAi is a Streamlit-based multifunctional AI chatbot tailored for learners, educators, and curious minds. It seamlessly integrates multimodal input, voice response, document summarization, diagram generation, and RAG-based document Q&A, all powered by modern LLMs like Groq and Mistral.

Github link:-

https://github.com/developer-Shaurya/ai_assistant

## 🚀 **Features**

### 🧠 Chatbot Powered by Groq LLMs</br>

- Dynamic, human-like conversations.</br>
- Option to choose models like `mistral-saba-24b` and `llama3-70b-8192`.

### 🎙️ Multimodal Input (MultimodInput.py)</br>

- Text: Regular chat input.</br>
- Voice: `Whisper model` transcribes spoken queries.</br>
- Image: `OCR-based` extraction using `Tesseract` for image-to-text questions.</br>

### 📊 Concept Diagram Generator (diagramgen.py)</br>

- Generate concept visualizations based on query context using LLM-driven classification and rendering libraries like `Graphviz` and `Matplotlib`.</br>
- Dynamically rendered inside the Streamlit app with download options.</br>

### 📄 PDF Summarizer (summarizer.py)</br>

- Upload any PDF and get concise summaries using Groq's `llama3-8b-8192`.</br>
- Built using `langchain`, `PyPDFLoader`, and `map_reduce summarization chains`.</br>

### 📚 RAG-based Document Q&A (rag_module.py)</br>

- Upload PDFs, DOCX, or TXT files.</br>
- Query content semantically using `FAISS`, `Sentence Transformers`, and `Groq`.</br>
- Context-aware response generation via `Retrieval-Augmented Generation`.</br>

### 🔈 Voice Output</br>

- Text responses can be read aloud using `ElevenLabs API` for immersive interaction.</br>

## 🛠️ Setup Instructions

1. Clone the Repository
<pre>
git clone https://github.com/developer-Shaurya/ai_assistant.git
cd ai_assistant
</pre>
2. Create a Virtual Environment
<pre>
  python -m venv venv
  source venv/bin/activate      # On Windows: venv\Scripts\activate
</pre>

3. Install Dependencies
<pre>
  pip install -r requirements.txt
</pre>

4. Setup Environment Variables
   Create a `.env` file:

<pre>
  GROQ_API_KEY=your_groq_api_key
  ELEVEN_API_KEY=your_elevenlabs_api_key
</pre>

Running the App

<pre>
  streamlit run chatbot.py
</pre>


## **2) 🤖 Agentic AI Chatbot**

Agentic AI Chatbot is an intelligent, dual-mode assistant that allows users to chat using either a basic LLM-powered chatbot or an advanced web-integrated chatbot. Built for flexibility, it supports multiple language models (like Groq, LLaMA, etc.) and offers up-to-date information retrieval via the Tavily Web Search API.

Render Deployment Link:-

https://agentic-ai-chatbot-1-b179.onrender.com/

Github link:-

https://github.com/Chiku91/Agentic-AI-Chatbot

✨ Key Features

🔹 Basic Chatbot Mode
Answers user queries using the selected LLM's internal knowledge base.

No external calls — ideal for static, factual, or conversational queries.

🔹 Advanced Search Mode
Fetches real-time information from the internet using Tavily API.

Useful for current events, news, or data not available in the LLM's training set.

🔹 LLM Selector
Choose your preferred model at runtime (e.g., Groq, LLaMA, etc.).

🚀 How It Works
Select Mode: Choose between Basic or Advanced Search.

Select LLM: Pick your desired language model.

Chat: Ask questions and get intelligent, relevant responses.

🔐 API Keys Required
OPENAI_API_KEY, TAVILY_API_KEY, etc. (managed via .streamlit/secrets.toml or .env).

**You have to enter your own Groq API key and Tavily API key.**

## **3) Personal AI Coach (Extra Feature)**

Github link:-  
https://github.com/Chiku91/Personal-AI-Coach
   
   🚀 ElevateU – AI-Powered Career Coach
ElevateU is a smart career coaching app built with Streamlit and OpenAI GPT-4 to help students and professionals boost their careers with AI-driven insights.

🔑 Key Features:

-> **Resume Matcher** – Upload your resume and match it to job descriptions with a detailed gap analysis.

-> **Skill Builder** – Get personalized learning paths based on your resume.

-> **Course Recommender** – Discover top online courses tailored to your interests.

-> **Career Path Explorer** – Generate skill roadmaps and hiring insights for your dream role.

-> **Mock Interview** – Practice with AI-generated questions and receive instant feedback.

-> **Hackathons & Internships** – Find relevant events and opportunities based on location.

-> **Industry Trends Map** – Explore region-specific tech and hiring trends interactively.

🔒 Secure by Design:
API keys are safely stored in .streamlit/secrets.toml and never exposed publicly.

**You have to enter your own OpenAI API key.**

Setup Environment Variables
   
   -> Create a .streamlit/ secrets. toml in your project folder

<pre>
  openai_key="sk-xxxxxxxxxxxxxxxxxxxxxxxxx"
</pre>

Running the App

<pre>
  streamlit run streamlit_app.py
</pre>

### **4) 🎓 Student Activity Detection System – Tracking Disengagement and Suggesting Adaptive Teaching Methods**

Kaggle Dataset link:-

https://www.kaggle.com/datasets/phamluhuynhmai/classroom-student-behaviors

Took reference from a popular kaggle dataset consisting of tracking student behaviour in classrooms. Consists of analysing different facial expression analysis and body gesture analysis to detect disengagement and suggest adapative teaching methods.

Github link:-

https://github.com/developer-Shaurya/Student-Activity-Detector

This project is a real-time computer vision-based system designed to **monitor and analyze student activities in the classroom** using

The system detects and visualizes multiple student behaviors such as **writing**, **raising hands**, **speaking**, **standing**, **head turning**, and even **teacher guidance**, with animated feedback messages to enhance interactivity.

**🎯 This system is used for student activity detection, tracks student disengagement or confusion using facial expression analysis, and suggests interventions using dynamic prompts and warnings.**

## 🔧 Tech Stack

- [✔️] **OpenCV** – Video capture, processing, and visual overlays
- [✔️] **YOLOv5 / YOLOv8** – Object detection (person, laptop, etc.)
- [✔️] **MediaPipe** – Hands, Face Mesh, Pose tracking
- [✔️] **PyTorch** – Deep learning model inference
- [✔️] **SoundDevice** – Audio volume detection
- [✔️] **Streamlit** – Web interface and module launcher

## 🚀 How It Works/ Module Overview

| Module | Description |
|--------|-------------|
| `activity.py` | 📚 Detects **writing** posture and forbidden objects (phone/laptop). Shows red warning animation. |
| `hand_raise.py` | ✋ Detects **raised hands** within person ROIs using MediaPipe Hands. |
| `speaking.py` | 🗣️ Detects **students speaking** using a combination of **audio volume** and **face location**. |
| `standing.py` | 🚶 Detects if students are **standing** (based on bounding box aspect ratio). |
| `teacher_guidance.py` | 🧑‍🏫 Detects **teacher guiding students** by checking for **standing posture, hand raise, and open mouth**. |
| `faceperson_detection.py` | 🧍 Combines **person detection** with **hand-raise detection** and shows encouraging animation. |
| `listening.py` | 👂 Tracks **student attention** using **face presence + movement tracking**. Also rotates visual aids like **charts, graphs, equations**. |
| `head_down_writing.py` | 📓 Detects students **writing with head down** posture. Shows a warning to sit upright. |
| `turning_head.py` | 👀 Detects if students **turn their head sideways/backward** for more than 5 seconds. |
| `main.py` | 🧠 Streamlit-based GUI to launch all the modules easily from a dropdown menu. |

## 🖥️ Streamlit Interface

Running the App

<pre>
  streamlit run main.py
</pre>



