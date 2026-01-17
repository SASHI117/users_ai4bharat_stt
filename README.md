# AI4Bharat STT Client

This repository contains a **client-side Python script** to send audio files to a
remote **AI4Bharat Speech-to-Text (STT) API** and receive transcriptions.

⚠️ **Important**:
This repo does **NOT** run any ML model locally.
The STT model runs on a **remote server**.

---

## ✅ Prerequisites

* Python **3.8 or higher**
* Internet connection
* Access to a **running STT API endpoint**

---

## 🔧 Installation

```bash
git clone https://github.com/<your-username>/ai4bharat-stt-client.git
cd ai4bharat-stt-client
pip install -r requirements.txt
```

---

## 🔑 Configuration (REQUIRED)

Before running the script, you **must edit** `stt_client.py` and set:

```python
API_URL = "YOUR_API_URL"
API_KEY = "YOUR_API_KEY"
```

### 🔹 What these mean

* **API_URL**
  The full URL of the running STT FastAPI service

* **API_KEY**
  The Bearer token required to authenticate with the API

⚠️ The script will **not work** unless both values are set correctly.

---

## ▶️ How to Run

```bash
python users.py
```

You will see a menu:

```
1️⃣  Single audio file
2️⃣  Folder with multiple audio files
```

Follow the prompts to provide:

* A single audio file path, **or**
* A folder containing multiple audio files

---

## 🎵 Supported Audio Formats

* `.wav`
* `.mp3`
* `.flac`
* `.m4a`
* `.ogg`

---

## 📤 Example Output

```json
{
  "filename": "sample.wav",
  "text": "A long fairy tale ...",
  "latency_ms": 3000.12
}
```

---

## 🧠 Notes

* No GPU required
* No Hugging Face setup needed
* No Azure access needed for client users
* Works on **Windows / Linux / macOS**
* Supports **batch transcription** via folders

---
