# TL;DW
Too Long; Didn't watch is an AI-powered Streamlit app that helps users digest long-form educational YouTube videos by summarizing the content and generating an interactive quiz from the transcript.  

**Watch the Live Demo:** [https://youtu.be/VYV_lgn4dSI?si=6VKQVNDe3Yg18xCF](https://youtu.be/VYV_lgn4dSI?si=6VKQVNDe3Yg18xCF)

<p align="center">
  <img src="quick_demo.gif" alt="App Demo" />
</p>


---

## How It's Made:

**Tech used:** Python, Streamlit, Whisper, Gemini (Google Generative AI), HuggingFace Summarizer, HTML/CSS (via Streamlit)

This project uses the `pytubefix` library to download audio from YouTube and `whisper` to transcribe spoken content to text. The transcript is then summarized using both extractive (`bert-extractive-summarizer`) and abstractive (`pysummarization`) techniques.

The standout feature is the **AI-generated quiz**, powered by Google's Gemini 2.0 Flash model, which parses the transcript and constructs multiple-choice questions. Users get instant feedback (correct/incorrect) and scores, creating a more active and engaging learning experience.

The frontend is built using **Streamlit**, providing a clean, responsive interface with embedded video, summaries, transcripts, and interactive quiz components.

---
## Optimizations

- Used streamlit sessions to persist user answers and prevent data loss between reruns.
- Prevented radio buttons from pre-selecting answers with `index=None`, forcing user engagement.
- Broke down Gemini prompt and response parsing logic into modular components to support future features like flashcard generation and answer explanations.
- Cached transcription and summarization logic for improved performance in terms of faster turn around time for the application.

---

## Lessons Learned

This project helped me learn how to **chain together multiple AI components** — transcription, summarization, and quiz generation — into a seamless pipeline. I also learned how to create a clean, responsive Streamlit interface that handles state changes well.

I gained valuable experience working with **real-world audio transcription** using Whisper, API integration with Google’s LLMs, and UX considerations for quiz interactivity.

---
