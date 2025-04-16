<div align="center">

# 🤖 MinerlexAI 💎

**AI-Powered Multilingual Assistant for Mining Law**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Python Version](https://img.shields.io/badge/python-3.8+-blue.svg)
![Framework](https://img.shields.io/badge/Framework-Streamlit-red.svg)

</div>

---

**MinerlexAI** simplifies understanding **Mining Laws** using AI. It combines **Google Gemini** for legal Q&A, **MBart** for translation, and **gTTS** for voice output, offering support in numerous Indian languages.

---

## ✨ Features

* 🧠 **AI Legal Assistant**: Leverages Google Gemini to answer mining law queries accurately.
* 🌍 **Multilingual Power**: Translates answers into 12+ Indian languages via MBart50.
* 🔊 **Text-to-Speech**: Converts text responses into clear audio using gTTS.
* 🎙️ **Voice Interaction**: Allows users to ask questions using their microphone.
* 📄 **PDF Ready**: UI prepared for PDF uploads (backend implementation pending).
* 💡 **Interactive & Smooth UI**: Built with Streamlit for a great user experience.

---

## 🛠️ Tech Stack

| Tool / Library                       | Purpose                     |
| :----------------------------------- | :-------------------------- |
| **Streamlit** | Interactive Web UI          |
| **Google Gemini** (`google.generativeai`) | Core Q&A Generation       |
| **MBart50** (HuggingFace Transformers) | Neural Machine Translation  |
| **gTTS** (Google Text-to-Speech)     | Speech Synthesis            |
| **SpeechRecognition** | Voice Input Processing      |
| **python-dotenv** | Environment Variables       |
| **PyTorch** | ML Model Backend (for MBart)|

---

## ⚙️ Application Workflow

This diagram shows how MinerlexAI processes user requests:

```mermaid
graph TD
    A[🗣️ User Input (Text/Voice)] --> B(🖥️ Streamlit Interface);

    subgraph "Input Processing"
        B -- If Voice --> C(🎤 Speech Recognition);
        C -- Text Query --> D[📝 Query Text];
        B -- If Text --> D;
    end

    subgraph "Core Logic"
        D --> E(🧠 Google Gemini API);
        E -- English Response --> F[📜 Raw Response];
    end

    subgraph "Output Processing"
        F --> G{🔄 Translate?};
        G -- Yes --> H(🌍 MBart Translation);
        H -- Translated Text --> I[✅ Final Text];
        G -- No (English) --> I;
        I --> J(📄 Display Text in UI);
        I --> K{🔊 Generate Audio?};
        K -- Yes --> L(🗣️ gTTS);
        L -- Audio Output --> M(🎶 Play Audio in UI);
    end

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style B fill:#ccf,stroke:#333,stroke-width:2px
    style E fill:#lightgrey,stroke:#333,stroke-width:2px
    style J fill:#cfc,stroke:#333,stroke-width:2px
    style M fill:#cfc,stroke:#333,stroke-width:2px
````

**Flow Explanation:**

1.  The user provides input (text/voice) via the **Streamlit Interface**.
2.  Voice input is converted to text using **Speech Recognition**.
3.  The query text is sent to the **Google Gemini API**.
4.  Gemini returns an English response.
5.  If requested, **MBart** translates the response.
6.  The final text (English or translated) is prepared.
7.  The text is **displayed** in the Streamlit UI.
8.  If requested, **gTTS** generates audio from the final text.
9.  The generated audio is made **playable** in the UI.

-----

## 📦 Installation Guide

1.  **Clone the Repository:**

    ```bash
    git clone [https://github.com/yourusername/minerlexai.git](https://github.com/yourusername/minerlexai.git)
    cd minerlexai
    ```

2.  **Set Up Virtual Environment** (Recommended):

    ```bash
    # Create environment
    python -m venv venv

    # Activate environment
    # Linux/macOS:
    source venv/bin/activate
    # Windows:
    # venv\Scripts\activate
    ```

3.  **Install Dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

    *(Ensure you have a `requirements.txt` file listing all needed packages)*

4.  **Configure Environment Variables:**
    Create a `.env` file in the root directory and add your API key:

    ```env
    # .env file
    GEMINI_API_KEY=YOUR_GOOGLE_GEMINI_API_KEY_HERE
    ```

-----

## 🚀 Run the Application

Execute the following command in your terminal:

```bash
streamlit run app.py
```

Navigate to the local URL provided by Streamlit (usually `http://localhost:8501`).

-----

## 🌐 Supported Languages

MinerlexAI supports translation to and from English for the following Indian languages (MBart codes):

  * Hindi (hi\_IN) - हिन्दी
  * Bengali (bn\_IN) - বাংলা
  * Tamil (ta\_IN) - தமிழ்
  * Telugu (te\_IN) - తెలుగు
  * Marathi (mr\_IN) - मराठी
  * Gujarati (gu\_IN) - ગુજરાતી
  * Malayalam (ml\_IN) - മലയാളം
  * Kannada (kn\_IN) - ಕನ್ನಡ
  * Odia (or\_IN) - ଓଡ଼ିଆ
  * Urdu (ur\_PK) - اردو *(Note: MBart uses Pakistan locale)*
  * Assamese (as\_IN) - অসমীয়া
  * *... potentially more supported by MBart50*

-----

## 📝 Important Notes

  * 🔑 **API Key**: A valid Google Gemini API key is essential. Get one from [Google AI Studio](https://aistudio.google.com/).
  * 🎤 **Microphone**: Browser permission is required for voice input functionality.
  * ⏳ **Model Download**: The MBart translation model (\~2.4 GB) will be downloaded automatically on first use. This may take some time.
  * 📄 **PDF Feature**: The PDF upload interface is present but requires backend development (parsing, embedding, RAG) to become functional.

-----

## 🙌 Contributing

Contributions make the open-source community amazing\! If you have ideas for improvements or find a bug:

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

Feel free to open an issue for discussion first\!

-----

## 📄 License

Distributed under the **MIT License**. See `LICENSE` file for more information.
*(Make sure you have a file named `LICENSE` in your repository)*

-----

\<div align="center"\>

## 👤 Author

Built with ❤️ by **Mrinal** | [GitHub Profile](https://github.com/Whisplnspace)

\</div\>
