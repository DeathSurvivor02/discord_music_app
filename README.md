# Discord Music Mobile App 📱🎶

A React Native & Expo mobile application companion for the [Discord Music Bot](https://github.com/DeathSurvivor02/discord_music_bot). Control your Discord music session, view now-playing tracks, manage queues, and watch real-time AI DJ commentary right from your phone.

---

## ✨ Features

- 🎧 **Now Playing & MiniPlayer**: Real-time track progress, play/pause, skip, volume slider, and repeat modes.
- 🎙️ **AI DJ Visualizer**: Live animated frequency bars and speech bubble reflecting the Spotify-style AI DJ commentary.
- 📜 **Queue Management**: Inspect upcoming tracks, clear the queue, or view history.
- ⚡ **Cross-Service Sync**: Communicates seamlessly with the Discord Bot's FastAPI backend (`api_server.py`) over REST and WebSockets.

---

## 🚀 Getting Started

### 1. Prerequisites
- **Node.js** (v18+)
- **Expo Go** app installed on iOS or Android

### 2. Installation
```bash
git clone https://github.com/DeathSurvivor02/discord_music_app.git
cd discord_music_app

npm install
```

### 3. Configure Bot API Endpoint
Ensure the companion bot backend (`api_server.py` in `discord_music_bot`) is running on port 8000:
- If testing locally on the same network, update `API_BASE_URL` in `src/services/api.js` to your computer's local IP (e.g. `http://192.168.1.X:8000`).
- If testing remotely or via tunneling, use your ngrok or domain URL.

### 4. Run the Mobile App
```bash
npx expo start
```
Scan the QR code with **Expo Go** (Android) or the **Camera app** (iOS).

---

## 🔄 Synchronization with Discord Bot

This repository is kept up to date with [discord_music_bot](https://github.com/DeathSurvivor02/discord_music_bot) via automated GitHub Actions repository dispatch events. When API endpoints or models update on the bot service, this repository receives automated sync notifications.
