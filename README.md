# BetterWeb – Adaptation Made Easy

A powerful Chrome extension designed to make the internet more accessible for users with ADHD, dyslexia, sensory sensitivities, visual impairments, and other cognitive conditions.

## 📌 Tagline

**Adaptation Made Easy.** Personalise the web in real-time with AI-powered accessibility.

---

## ⚠️ Problem Statement

The web today isn't built for everyone. Millions of users with cognitive and sensory disabilities are excluded by rigid, inaccessible design. This limits access to education, services, and opportunities.

---

![BetterWeb Screenshot](https://github.com/user-attachments/assets/89709e8c-378f-49b6-9052-30e2cc9f7022)

---

## 💡 Our Solution

**BetterWeb** is a Chrome extension that empowers users to personalise their browsing experience using AI-driven accessibility tools. Whether it’s reducing sensory overload, enabling voice control, or adjusting visuals, BetterWeb adapts websites to each user’s needs.



## 🌟 Key Features

### ✨ Accessibility Profile Setup
Upon installation, users complete a simple three-step form to specify their disabilities/preferences (e.g., ADHD, dyslexia).

### 🔊 Text-to-Speech (TTS)
Highlight text and right-click to have it read aloud.

### 🎨 Theming System
Choose from soft pastel themes (lavender, mint, peach) to reduce overstimulation—designed especially for autism spectrum users.

### ⚙️ Options Page Interface
Dedicated settings for:
- Visual Disabilities
- Dyslexia
- ADHD
- Photosensitivity
- Cognitive Needs
- Motion Sensitivity

### 🤖 AI Assistant & Talking Bot
Natural language chatbot to guide users, trigger features, or explain tools—all hands-free.

---

## 📋 Table of Contents
- [Installation](#installation)
- [Chrome Extension Setup](#chrome-extension-setup)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)

---

## 🚀 Installation

### Prerequisites
- **Chrome Browser** (or any Chromium-based browser)
- **Python 3.8+** (for AI agent backend)
- **Node.js** (optional, for frontend development)

### Step 1: Clone or Download the Repository
```bash
git clone https://github.com/Dhruv-Gupta014/better_web_main.git
cd better_web-main
```

### Step 2: Install Python Dependencies (For AI Agent)
```bash
pip install -r requirements.txt
```

If `requirements.txt` doesn't exist, manually install:
```bash
pip install flask flask-cors python-dotenv
```

---

## 🔧 Chrome Extension Setup

### Method 1: Load Extension in Developer Mode (Recommended for Development)

1. **Open Chrome and go to Extensions Page:**
   - Type `chrome://extensions/` in the address bar, or
   - Go to Menu → More Tools → Extensions

2. **Enable Developer Mode:**
   - Toggle the **"Developer mode"** switch in the top-right corner

3. **Load the Extension:**
   - Click **"Load unpacked"**
   - Navigate to one of these folders:
     - `BetterWeb/` (Main version)
     - `FINAL/` (Final polished version)
     - `Webease/` (Alternative UI)
     - `color blind/` (Color-blind friendly variant)
   - Click **"Select Folder"**

4. **Verify Installation:**
   - The extension should appear in your Chrome toolbar
   - Click the extension icon to open the popup

### Method 2: Package as .crx File (For Distribution)

1. In `chrome://extensions/`, right-click your loaded extension
2. Select **"Pack extension"**
3. Choose the extension folder and create a private key
4. A `.crx` file will be generated

---

## ▶️ Getting Started

### Starting the Chrome Extension

1. **Open the Extension:**
   - Click the BetterWeb icon in your Chrome toolbar
   - The popup should load

2. **Complete Setup (First Time):**
   - Fill out the accessibility profile form
   - Select your preferences (ADHD, Dyslexia, Visual Impairments, etc.)
   - Choose a theme (Lavender, Mint, Peach)
   - Click "Save Settings"

3. **Use the Features:**
   - **Text-to-Speech:** Highlight any text on a webpage → Right-click → "Speak"
   - **Theme Application:** Settings automatically apply to all websites
   - **AI Chatbot:** Click the chatbot icon in the popup to ask questions

### Starting the AI Agent (Backend)

1. **Navigate to the AI agent folder:**
   ```bash
   cd Aiagent
   ```

2. **Run the main agent:**
   ```bash
   python main.py
   ```
   or
   ```bash
   python frontend.py
   ```

3. **The agent will start listening for requests** from the extension

---

## 📁 Project Structure

```
better_web-main/
├── BetterWeb/                 # Main Chrome extension
│   ├── manifest.json          # Extension configuration
│   ├── popup.html/js          # Popup interface
│   ├── content.js             # Content script (injects into webpages)
│   ├── background.js          # Background service worker
│   ├── options.html/js        # Settings page
│   └── googleTTS.js           # Text-to-Speech implementation
│
├── FINAL/                     # Production-ready version
│   ├── popup.html/js
│   ├── content.js
│   └── manifest.json
│
├── Webease/                   # Alternative UI version
├── color blind/               # Accessibility variant
├── Aiagent/                   # Python AI backend
│   ├── main.py                # Main agent logic
│   ├── frontend.py            # Frontend interface
│   └── recordings/            # Audio recordings
│
├── Html/                      # Static HTML pages
├── fs/                        # File system utilities
├── README.md
└── agent.py                   # Main agent entry point
```

---

## 🛠️ Technologies Used

- **Frontend:** HTML, CSS, JavaScript
- **Chrome APIs:** Content Scripts, Background Workers, Storage API
- **Backend:** Python, Flask
- **AI/NLP:** Natural language processing for chatbot
- **Audio:** Google Text-to-Speech API, Web Audio API
- **Styling:** CSS3 with accessibility-focused design

---

## 🎯 Features Explained

| Feature | How to Use |
|---------|-----------|
| **Text-to-Speech** | Highlight text → Right-click → "Speak" |
| **Theme Changer** | Open popup → Select theme from dropdown |
| **ADHD Mode** | Reduces animations, simplifies layouts |
| **Dyslexia Mode** | Uses dyslexia-friendly fonts (OpenDyslexic) |
| **Dark Mode** | Reduces eye strain for photosensitive users |
| **AI Chatbot** | Click chatbot icon to ask questions |

---

## 🔐 Permissions Requested

The extension requests these permissions for functionality:
- `activeTab` - Interact with current webpage
- `scripting` - Inject content scripts
- `storage` - Save user settings
- `tts` - Text-to-Speech functionality

---

## 🐛 Troubleshooting

### Extension not loading?
- Ensure you're using the latest Chrome version
- Check that Developer Mode is enabled
- Try clicking "Reload" on the extension card

### Text-to-Speech not working?
- Check browser audio settings
- Ensure Google TTS API is configured
- Try reloading the extension

### AI Agent not responding?
- Verify Python dependencies are installed
- Check that `main.py` is running
- Look for error messages in browser console (F12)

---

## 📝 License
This project is open-source and available under the MIT License.

---

## 👥 Contributing
Contributions are welcome! Please feel free to submit issues and pull requests.

---

## 📧 Support
For issues, questions, or suggestions, please open an issue on GitHub or contact the development team.

### 🖼️ AI-Based Image Color Correction *(Prototype Phase)*
Uses generative AI to adapt image contrast for various types of colour blindness.

### 🕹️ Motion Sensitivity Support
Voice command and head-tracking (using TensorFlow.js / MediaPipe) for hands-free navigation.

###  Learning Platform *(Planned)*
Auto-adaptive UI based on a user’s profile, offering inclusive course delivery.

---

##  Tech Stack
-**Ai Agent -> streamlit,web scraping using ChatGenerative Embeddings, GoogleGenerative Ai, BrwoserUse
- **Frontend:** HTML, CSS, JavaScript, React.js, TailwindCSS
- **Chrome APIs:** Manifest V3, Chrome Storage
- **AI & Tools:** Cohere API (v2), Google TTS, OpenCV, PyTesseract, FFmpeg, PyQt5
- **Other:** JSON Dataset, DOM Manipulation

---

##  Revenue Model

**Freemium:**
- Basic tools: Themes, TTS, profile setup
- Limited chatbot & manual control

**Premium (Subscription):**
- Advanced chatbot (unlimited NLP)
- Auto-mode, color correction
- Cloud sync & customized courses

---

##  Future Plans
- Full generative color-enhancement
- Real-time accessibility audit engine
- Cloud-based syncing across devices
- More granular accessibility triggers




---

## 👥 Team
- **Shaurya Tyagi**
- **Kavya kapoor**
- **Lakshya Gupta**


#   b e t t e r _ w e b _ m a i n 
 
 