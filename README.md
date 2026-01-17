# AI4Bharat STT Client

This repository contains a **client-side Python script** to send audio files to a
remote **AI4Bharat Speech-to-Text (STT) API** and receive transcriptions.

⚠️ **Important**:
This repo does **NOT** run any ML model locally.
The STT model runs on a **remote server** (for example, an Azure VM).

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
API_URL = "http://<YOUR_VM_PUBLIC_IP>:8000/stt"
API_KEY = "<YOUR_API_KEY>"
```

### 🔹 What these mean

* **API_URL**
  The full URL of the running STT FastAPI service
  Example:

  ```
  http://74.225.216.132:8000/stt
  ```

* **API_KEY**
  The Bearer token required to authenticate with the API
  Example:

  ```
  ai4bharat-secret-key-6262
  ```

⚠️ The script will **not work** unless both values are set correctly.

---

## ▶️ How to Run

```bash
python stt_client.py
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
  "text": "మేడం నాకు వచ్చింది ...",
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

## ⚠️ Security Note

Do **NOT** commit real API keys to public repositories.
If sharing this repo publicly, replace the key with a placeholder.

---

## 📌 Author

**Sashi Vardhan Pragada**

---

If you want next, I can:

* Move `API_URL` and `API_KEY` to a `.env` file
* Add CLI flags instead of editing code
* Add CSV / JSON output saving
* Make a Windows `.exe`

Just tell me what you want next 🚀
