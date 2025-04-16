
```markdown
# 🤖 MinerlexAI

**MinerlexAI** is an AI-powered multilingual assistant designed to simplify and revolutionize the understanding of **Mining Laws**. It leverages **Google Gemini** for legal Q&A, **MBart** for neural machine translation, and **gTTS** for voice synthesis — providing mining law support in multiple Indian languages with voice playback.

---

## 🚀 Features

- 🧠 **AI-Powered Legal Assistant**: Uses Gemini (Google's LLM) to understand and answer mining law-related queries.
- 🌍 **Multilingual Support**: Translates responses into 12+ Indian languages using Facebook's MBart50 model.
- 🔊 **Text-to-Speech**: Converts translated responses into speech using Google Text-to-Speech (gTTS).
- 🎙️ **Speech Input**: Users can interact using voice commands via microphone.
- 📄 **PDF Upload Ready**: Upload PDFs to extend functionality (in development).
- 💡 **Interactive UI**: Built with Streamlit for a seamless web experience.

---

## 🛠️ Tech Stack

| Tool / Library      | Usage                                   |
|---------------------|------------------------------------------|
| Streamlit           | Web UI                                  |
| Google Gemini (via `google.generativeai`) | Q&A Generation |
| MBart50 (HuggingFace) | Language Translation                  |
| gTTS (Google Text-to-Speech) | Audio generation              |
| SpeechRecognition   | Voice input                             |
| dotenv              | Environment configuration                |
| PyTorch             | Backend for MBart model                  |

---

## 📦 Installation

1. **Clone the repository:**

```bash
git clone https://github.com/yourusername/minerlexai.git
cd minerlexai
```

2. **Create a virtual environment (optional but recommended):**

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies:**

```bash
pip install -r requirements.txt
```

4. **Set up your `.env` file:**

```env
GEMINI_API_KEY=your_google_gemini_api_key
```

---

## 🧪 Run the App

```bash
streamlit run app.py
```

---

## 🌐 Supported Languages

- English
- Hindi (हिन्दी)
- Bengali (বাংলা)
- Tamil (தமிழ்)
- Telugu (తెలుగు)
- Marathi (मराठी)
- Gujarati (ગુજરાતી)
- Malayalam (മലയാളം)
- Kannada (ಕನ್ನಡ)
- Odia (ଓଡ଼ିଆ)
- Urdu (اردو)
- Assamese (অসমীয়া)

---

## 🔒 Notes

- **Google Gemini** API access is required.
- **Microphone access** must be granted to use speech input.
- PDF functionality is available as a UI element but can be expanded for document parsing.

---

## 🙌 Contributing

Pull requests are welcome! If you find a bug or have suggestions for improvements, feel free to open an issue.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👤 Author

Built with ❤️ by [Mrinal](https://github.com/Whisplnspace)

```

---

Let me know if you'd like a logo, deployment guide (e.g. for Hugging Face Spaces or Streamlit Cloud), or `requirements.txt` content!
