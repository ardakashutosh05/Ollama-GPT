# 🧠 Ollama-GPT — Self-Hosted Private LLM with Open WebUI

Run your own **ChatGPT-like interface** entirely offline using:
- **[Ollama](https://ollama.com/)** — Run AI models locally on your own machine.
- **[Open WebUI](https://github.com/open-webui/open-webui)** — Beautiful ChatGPT-style interface.

> ⚡ **Privacy-first**: No API keys, no data sharing — 100% offline.

---

## 📦 Features
- 🚀 Run open-source LLMs locally (LLaMA, CodeLLaMA, Qwen, Phi, etc.)
- 🔒 Fully private — your data stays on your machine
- 🐳 Docker-based setup for quick deployment
- 💻 CLI or Web UI access
- ⚙ Configurable CPU & RAM limits

---

## 🚀 Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/ashubambal/ollama-gpt.git
cd ollama-gpt
```

### 2️⃣ Configure Environment Variables (Optional)
Edit docker-compose.yml and set your own WEBUI_SECRET_KEY:
```bash
WEBUI_SECRET_KEY=enter-your-secret-key
```

### 3️⃣ Start the Containers
```bash
docker compose up -d
```

### 4️⃣ Verify Running Containers
```bash
docker ps
```
Expected:

- ollama — AI model server
- open-webui — Web interface


### 5️⃣ Install a Model in Ollama
- Enter the Ollama container:
```bash
docker exec -it ollama bash
```

- Pull a model (example: llama3.2:1b-instruct-q4_0):
```bash
ollama pull llama3.2:1b-instruct-q4_0
```

- Test in CLI:
```bash
ollama run llama3.2:1b-instruct-q4_0
```

### 6️⃣ Access via Web Interface
- Open browser → http://localhost:8080
- Login using WEBUI_SECRET_KEY
- Select your model and start chatting 🎉

### 📚 Model Resources
- Ollama Model Library
- Recommended code-focused models:
    - codellama
    - qwen2.5-coder
    - phi3.5

### 🎥 Output Demo

<p align="center">
  <img src="assets/demo.gif" alt="Demo" width="700">
</p>

### 🛠 Stopping the Services
```bash
docker compose down
```

### 📄 License
MIT — Free to use and modify.
```bash
 
This is **one continuous README** — no separated instructions, everything from install to demo is inside.  

If you want, I can now **add screenshots of the Open WebUI UI** directly into this same README so that new users see exactly what they’ll get before running it.  

Do you want me to add those screenshots in this file?

```
