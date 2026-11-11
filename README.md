# 🤖 AI Study Assistant

An AI-powered study assistant built with Python, Gradio, and Google's Gemini API. It helps users understand study-related questions through AI-generated explanations with two selectable response personalities: **Friendly** and **Academic**.

## 📌 Project Overview

The AI Study Assistant provides an interactive interface where users can enter questions and receive AI-generated responses.

Users can select how the AI communicates:

- **Friendly Mode:** Provides encouraging, beginner-friendly explanations using analogies and real-world examples.
- **Academic Mode:** Provides more formal, detailed, and academically oriented explanations.

The application uses Google's Gemini API to generate responses based on the selected personality instructions.

## ✨ Features

- Interactive web interface built with Gradio.
- AI-powered question answering using Google's Gemini API.
- Two selectable AI personalities.
- Beginner-friendly explanations.
- Real-world examples and analogies.
- Configurable AI generation parameters.
- Simple Python-based implementation.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core application development |
| Gradio | Interactive user interface |
| Google GenAI SDK | Gemini API integration |
| Gemini | AI response generation |
| Environment Variables | Secure API key configuration |

## 🏗️ Project Architecture

```text
AI-Study-Assistant/
│
├── app.py
│   ├── Import required libraries
│   ├── Initialize Gemini API client
│   ├── Define AI personalities
│   ├── Define study_assistant() function
│   ├── Configure Gemini generation
│   ├── Build Gradio interface
│   └── Launch application
│
├── requirements.txt
│   └── Project dependencies
│
└── README.md
    └── Project documentation
```

## ⚙️ How It Works

The application follows a simple workflow:

### 1. User Input

The user enters a study-related question into the Gradio textbox.

### 2. Personality Selection

The user selects one of the available AI personalities:

- Friendly
- Academic

### 3. System Prompt Selection

The Python application retrieves the system instruction associated with the selected personality from the `personalities` dictionary.

### 4. Gemini API Integration

The `study_assistant()` function sends the user's question and selected system instruction to Google's Gemini model using the Google GenAI SDK.

### 5. AI Response Generation

The configured model generates a response using the following parameters:

- Model: `gemini-3.5-flash-lite`
- Temperature: `0.4`
- Maximum output tokens: `2000`

### 6. Response Display

The generated response is returned to the Gradio interface and displayed in the output textbox.

## 📂 Core Application Components

### `app.py`

The main application file contains the complete application logic.

**Important components:**

- `genai.Client()` – Initializes the Google GenAI client using the API key from the environment.
- `personalities` – Stores the Friendly and Academic system instructions.
- `study_assistant()` – Processes user questions, selects the personality, calls Gemini, and returns the response.
- `gr.Interface()` – Creates the interactive application interface.
- `demo.launch()` – Starts the Gradio application.

### `requirements.txt`

Contains the Python dependencies:

```text
gradio
google-genai
```

## 🚀 Installation and Setup

### Prerequisites

- Python installed.
- Git installed.
- Google Gemini API key.

### Step 1: Clone the Repository

```bash
git clone https://github.com/Narsimulu-G/AI-Study-Assistant.git
```

### Step 2: Navigate to the Project

```bash
cd AI-Study-Assistant
```

### Step 3: Create a Virtual Environment

```bash
python -m venv venv
```

Activate it on Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

### Step 4: Install Dependencies

```bash
python -m pip install -r requirements.txt
```

### Step 5: Configure Gemini API Key

Set your API key as an environment variable in Windows PowerShell:

```powershell
$env:GEMINI_API_KEY="YOUR_GEMINI_API_KEY"
```

Replace `YOUR_GEMINI_API_KEY` with your actual API key.

Never upload your API key to GitHub.

### Step 6: Run the Application

```bash
python app.py
```

The Gradio application will start. Open the local URL displayed in your terminal to interact with the Study Assistant.

## 🔐 Security

- The Gemini API key is accessed through an environment variable.
- Do not hardcode API keys in the source code.
- Do not commit `.env` files or other files containing secrets.

## 🔮 Future Improvements

Potential enhancements include:

- Study notes summarization.
- PDF document question answering.
- Quiz and practice question generation.
- Conversation history.
- Subject-specific learning modes.
- Improved error handling and API response validation.

These are planned enhancements and are not currently implemented.

## 👨‍💻 Author

**G Narsimulu**
