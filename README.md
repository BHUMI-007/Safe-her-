# 🛡️ SafeHer — AI-Powered Women's Safety Companion

> *"Because every woman deserves to feel safe."*

[![Live Demo](https://img.shields.io/badge/Live-Demo-purple)](https://safeher-28bb2.web.app)
[![Backend](https://img.shields.io/badge/Backend-Render-green)](https://safeher-0x4u.onrender.com)
[![Firebase](https://img.shields.io/badge/Database-Firebase-orange)](https://firebase.google.com)
[![Elite Her](https://img.shields.io/badge/Elite%20Her-Hackathon%20Finalist-pink)](https://www.eliteher.xyz)

---

## 🌟 What is SafeHer?

SafeHer is an AI-powered Progressive Web App (PWA) designed to be a real-time personal safety companion for women. It combines one-tap SOS with real phone calls, Gemini AI risk scoring, voice distress detection, live trip monitoring, an emotional support AI chatbot (Sakhi), and community danger reporting — all completely free, no app download needed.

Selected as a **finalist at Elite Her Hackathon 2026**.

---

## ✨ Features

| Feature | Description | Status |
|---|---|---|
| 🆘 One-Tap SOS | Real phone calls + SMS to trusted contacts via Twilio | ✅ Live |
| 📍 Live Tracking | Real-time location sharing via Firebase | ✅ Live |
| 🤖 AI Risk Score | Gemini AI analyzes safety based on location & time | ✅ Live |
| 🎙️ Voice Detection | Detects distress words in Hindi & English ("help", "bachao") | ✅ Live |
| 🗺️ Safe Routes | AI-powered route safety analysis with map visualization | ✅ Live |
| 🔴 Danger Heatmap | Community reported unsafe areas on live map | ✅ Live |
| 🚶 Trip Monitor | Share live trip with contacts + auto-alert if overdue | ✅ Live |
| 💜 Sakhi Chatbot | AI emotional support companion in Hindi/English/Hinglish | ✅ Live |
| 🤫 Silent Decoy | Fake calculator screen while secretly sending SOS | ✅ Live |
| 📵 Offline PWA | Core features work without internet via Service Worker | ✅ Live |
| 👥 Trusted Circle | Save emergency contacts with Firebase sync | ✅ Live |
| 🔐 Phone Login | OTP-based authentication via Firebase | ✅ Live |
| 📳 Shake Detection | 3 shakes triggers voice verification then SOS | ✅ Live |

---

## 🚀 Live Demo

🌐 **Web App:** https://safeher-28bb2.web.app
📱 **Install as PWA:** Open in Chrome → Add to Home Screen
🔧 **Backend API:** https://safeher-0x4u.onrender.com

> ⚠️ Backend is on Render free tier — first request may take 50s to wake up.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript, PWA |
| Backend | Python, Flask, Gunicorn |
| Database | Firebase Realtime Database |
| Auth | Firebase Phone Authentication |
| AI | Google Gemini Pro |
| Calls & SMS | Twilio Voice + Messaging |
| Maps | Leaflet.js + OpenStreetMap + Nominatim |
| Hosting | Firebase Hosting + Render.com |

---

## 📁 Project Structure

```
SafeHer/
├── frontend/
│   ├── index.html        # Main app + SOS dashboard
│   ├── login.html        # Phone OTP login
│   ├── map.html          # Live safety map + Sakhi chatbot + Trip Monitor
│   ├── track.html        # Live location tracking page
│   ├── 404.html          # Error page
│   ├── script.js         # Core app logic
│   ├── style.css         # Styling
│   ├── manifest.json     # PWA manifest
│   └── sw.js             # Service worker (offline support)
├── backend/
│   ├── app.py            # Flask API (all routes)
│   ├── requirements.txt  # Python dependencies
│   └── Procfile          # Render deployment config
└── firebase.json         # Firebase hosting config
```

---

## ⚙️ API Endpoints

| Endpoint | Method | Description |
|---|---|---|
| `/api/sos` | POST | Trigger SOS — real Twilio calls + SMS |
| `/api/sos/cancel` | POST | Cancel active SOS |
| `/api/danger-zones` | GET | Get all reported danger zones |
| `/api/danger-zones/report` | POST | Report a new danger zone |
| `/api/ai/risk-score` | POST | AI safety risk assessment |
| `/api/ai/checkin` | POST | AI check-in message |
| `/api/ai/analyze-route` | POST | AI safe route analysis |
| `/api/ai/voice-alert` | POST | Voice distress detection |
| `/api/ai/chat` | POST | Sakhi AI chatbot conversation |
| `/api/trip/start` | POST | Start trip monitoring + notify contacts |
| `/api/trip/update` | POST | Update live location during trip |
| `/api/trip/end` | POST | End trip (safe/unsafe) |
| `/api/trip/<id>` | GET | Get trip status |
| `/api/movement/track` | POST | Track movement anomalies |
| `/api/contacts` | POST | Save emergency contacts |

---

## 🏃 How to Run Locally

### Backend:
```bash
cd backend
pip install -r requirements.txt

# Create .env file
cp .env.example .env
# Fill in your API keys

python app.py
```

### Frontend:
```bash
cd frontend
# Open index.html in browser
# Or use Live Server in VS Code
```

### Environment Variables (`backend/.env`):
```
TWILIO_ACCOUNT_SID=your_sid
TWILIO_AUTH_TOKEN=your_token
TWILIO_PHONE_NUMBER=your_twilio_number
GEMINI_API_KEY=your_gemini_key
```

> ⚠️ Never commit `.env` to GitHub. It is already in `.gitignore`.

---

## 🤖 How AI is Used

1. **Gemini AI Risk Scoring** — Analyzes location, time, and day → real-time safety score (1-10)
2. **Voice Distress Detection** — Detects Hindi + English distress words with confidence score → auto SOS if >80%
3. **Route Safety Analysis** — Evaluates journey safety, lists concerns and tips before travel
4. **Sakhi Chatbot** — Empathetic AI companion for emotional support in Hindi/English/Hinglish
5. **Anomaly Detection** — Detects unusual movement patterns from historical data

---

## 💡 How SafeHer is Different

| Feature | SafeHer | Other Apps |
|---|---|---|
| Real phone calls | ✅ Twilio Voice | ❌ Notification only |
| AI risk scoring | ✅ Gemini Pro | ❌ |
| Hindi voice detection | ✅ | ❌ |
| Trip monitoring | ✅ Live tracking link | ❌ |
| AI emotional support | ✅ Sakhi chatbot | ❌ |
| Works offline | ✅ PWA | ❌ |
| No app download | ✅ Browser-based | ❌ |
| Free to use | ✅ | Paid |
| Community heatmap | ✅ | ❌ |

---

## 🔮 Future Plans

- 🌐 Custom domain deployment (safe-her.xyz)
- 🌍 10+ Indian language support
- 📱 Native Android app
- ⌚ Smartwatch / wearable integration
- 🚔 Police department API integration
- 🏫 NGO & college safety partnerships
- 📡 True offline SMS via satellite

---

## 📜 License & Open Source

Licensed under **MIT License** — free to use, modify, and distribute.

### Dependencies Used:
- **Flask** — MIT License
- **Firebase SDK** — Apache 2.0
- **Twilio SDK** — MIT License
- **Google Generative AI** — Apache 2.0
- **Leaflet.js** — BSD 2-Clause
- **Flask-CORS** — MIT License

---

## 🏆 Hackathon

| Hackathon | Result |
|---|---|
| Elite Her Hackathon 2026 | 🏅 Finalist |

---

## 👩‍💻 Author

Built with 💜 by **Bhoomi** — Student Developer, Ashoka University

> SafeHer — AI that cares, technology that protects.