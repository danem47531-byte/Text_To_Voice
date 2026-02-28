# 🔊 Text To Voice — Python Mini Project

![Python](https://img.shields.io/badge/Language-Python-3776AB?logo=python&logoColor=white) ![Jupyter](https://img.shields.io/badge/Tool-Jupyter%20Notebook-F37626?logo=jupyter&logoColor=white) ![gTTS](https://img.shields.io/badge/Library-gTTS-FF6B6B) ![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📌 Project Overview

This is a simple yet practical **Text-to-Speech (TTS)** mini project built in Python using the **gTTS (Google Text-to-Speech)** library. It converts any written text into a spoken audio file (`.mp3`) and plays it directly inside Jupyter Notebook using a built-in audio player.

The project supports **multiple languages** including English, Hindi, French, Spanish, and Bengali — making it useful for multilingual applications.

---

## 🛠️ Library Used

```python
from gtts import gTTS
from IPython.display import Audio
```

| Library | Purpose |
|---|---|
| `gTTS` | Converts text to speech using Google's Text-to-Speech API |
| `IPython.display.Audio` | Plays the generated audio file directly inside Jupyter Notebook |

---

## 🚀 How It Works

The project follows a simple **3-step pipeline:**

```
Text Input → gTTS Converts to Audio → MP3 Saved & Played in Notebook
```

### Step 1 — Install gTTS
```python
!pip install gtts
```

### Step 2 — Convert Text to Speech
```python
from gtts import gTTS

text = "Hi my name is Tridev Pal"
tts = gTTS(text=text, lang='hi')  # lang='hi' for Hindi
tts.save("demo_audio.mp3")

print("Audio file saved as demo_audio.mp3")
```

### Step 3 — Play Audio in Jupyter Notebook
```python
from IPython.display import Audio

Audio("demo_audio.mp3")
```

This renders a **built-in audio player** directly in the notebook cell — no external media player needed!

---

## 🌍 Supported Languages

| Language | Code |
|---|---|
| English | `'en'` |
| Hindi | `'hi'` |
| French | `'fr'` |
| Spanish | `'es'` |
| Bengali | `'bn'` |

Simply change the `lang` parameter to switch between languages:
```python
tts = gTTS(text=text, lang='en')   # English
tts = gTTS(text=text, lang='hi')   # Hindi
tts = gTTS(text=text, lang='bn')   # Bengali
```

---

## 💡 Use Cases

- 🎓 **E-learning** — Convert study notes or lessons into audio
- ♿ **Accessibility** — Help visually impaired users consume text content
- 🌐 **Multilingual apps** — Generate voice output in multiple languages
- 📢 **Announcements** — Convert text announcements into audio files
- 🤖 **Voice bots** — Use as a base for building voice-enabled chatbots
- 📖 **Audiobook creation** — Convert written content into spoken audio

---

## 📁 Project Files

```
📦 Text To Voice
 ┗ 📓 Text_To_Voice.ipynb    # Jupyter Notebook with full implementation
```

---

## ▶️ How to Run

1. Clone this repository
2. Install the required library:
   ```bash
   pip install gtts
   ```
3. Open `Text_To_Voice.ipynb` in **Jupyter Notebook** or **VS Code**
4. Run all cells from top to bottom
5. The audio player will appear in the last cell — press **Play** to hear the output

---

## ⚠️ Common Issues & Fixes

| Problem | Fix |
|---|---|
| `ModuleNotFoundError` | Run `!pip install gtts` in the first cell |
| Audio not playing automatically | Use `Audio("demo_audio.mp3", autoplay=True)` |
| Want slower speech | Add `slow=True` → `gTTS(text=text, lang='en', slow=True)` |
| File not found error | Check working directory: `import os; print(os.getcwd())` |
| No internet connection | gTTS requires an active internet connection to work |

---

## 👤 Author

### Tridev Pal
📍 Calcutta, West Bengal, India

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?logo=linkedin)](https://www.linkedin.com/in/tridev-pal-74575a379/)

>Feel free to connect on LinkedIn or raise issues via GitHub if you have any suggestions or improvements!
