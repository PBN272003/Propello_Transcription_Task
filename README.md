# 🎙️ Propello Transcription Task

This project takes an audio file (like a phone call or meeting), splits the speech by speakers, turns it into readable text, and generates a professional transcript document — formatted just like real-world meeting notes.

It uses OpenAI's Whisper for transcription, Gemini Flash 1.5 for structured output generation, and Python for gluing it all together.

---

## 📁 Project Structure
     Propello_Transcription_Task/
    ├── Propello_assign1.ipynb # Jupyter notebook with complete workflow
    ├── reference_transcript.docx # Reference format for Gemini output
    ├── requirements.txt # All dependencies listed here
    ├── README.md # This file
    ├── output/ # Auto-generated transcript or docx files
    └── audio/ # Input audio files to transcribe

---

---

## ✅ What This Project Does

You can:

- Load and transcribe audio using Whisper
- Perform speaker diarization (differentiate speakers)
- Convert the transcription into a JSON format
- Use Gemini Flash 1.5 to reformat the text into a clean transcript
- Save the transcript as a `.docx` file in a formal, readable format
- Preview and interact with everything via a simple **Streamlit app**
- Share the app temporarily online using **ngrok**

---

## 🔧 Tech Used

- **Python 3.10+**
- [**Whisper by OpenAI**](https://github.com/openai/whisper)
- **Google Generative AI (Gemini 1.5 Flash)**
- **Torch, torchaudio**
- **ffmpeg-python**
- **python-docx** for creating Word files
- **Streamlit** for a user-friendly interface
- **ngrok** to expose the app on a public URL (handy for demos or testing)

---

## 📦 Dependencies

Install them all using:

```bash
pip install -r requirements.txt
```

The file includes:
```bash
  git+https://github.com/openai/whisper.git
  openai
  torch
  torchaudio
  ffmpeg-python
  google-generativeai
  python-dotenv
  ngrok
  streamlit
```

> `google-generativeai` is required for Gemini Flash 1.5 interaction.

---

## 🛠 How It Works (Behind the Scenes)

1. **Input**: You place an audio file (say `.mp3` or `.wav`) into the `audio/` folder.

2. **Transcription**: Whisper converts that audio into raw text and detects who is speaking and when.

3. **Diarization**: The script processes Whisper’s output to label parts as Speaker 1, Speaker 2, etc.

4. **Prompting Gemini**: The labeled conversation is sent to Gemini Flash 1.5 with a prompt asking it to match a reference `.docx` style.

5. **Output**: Gemini sends back a clean version, which is saved as a `.docx` file using `python-docx`.

6. **Streamlit Preview**: You can view and test the whole workflow using the built-in web interface powered by Streamlit.

7. **Public Link**: Want to share it online? Just run ngrok to get a public URL for your Streamlit app.


   

---

## ✍️ How to Use It

1. Clone the repo:
```bash
git clone https://github.com/PBN272003/Propello_Transcription_Task.git
cd Propello_Transcription_Task
```

## 🧠 Notes

- Whisper handles transcription with pretty good accuracy.
- Gemini Flash reformats the raw conversation into a formal structure.
- The speaker names are basic (Speaker 1, Speaker 2), but can be customized if diarization data is available.
- You can change the reference document (`reference_transcript.docx`) to control the format of the final output.
- Streamlit adds an optional interface for quick testing or demos.
- ngrok helps if you want to share your app without deploying to a cloud server.



---
![Transcription](https://github.com/user-attachments/assets/8b84e5bd-c75c-438f-a5cf-57d426f5a713)
