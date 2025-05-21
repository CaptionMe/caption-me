# CaptionMe 🎧🔍️🔮

**Live AI/ML-Powered Captions in AR for the Deaf/HoH**

CaptionMe is an assistive mobile app that connects to Roger microphones and AR smart glasses to deliver **real-time speech-to-text captions** anchored near speakers' mouths. It uses on-device AI/ML to provide an accessible communication solution for Deaf and Hard-of-Hearing users, allowing them to follow conversations spatially and naturally.

---

## 🌐 Project Overview

CaptionMe provides:

* Real-time **audio capture** from Roger wireless microphones
* Seamless **audio streaming** from a Raspberry Pi to a smartphone
* **Speech recognition** using offline or cloud-based models
* **Visual tracking** of speakers using the phone camera
* Dynamic **caption overlay placement** aligned to speakers' faces
* Delivery of live captions to AR glasses over Bluetooth/Wi-Fi

---

## 🧬 Key Features

* ✅ Live captions transcribed from real-world conversations
* 🏛️ Multi-speaker tracking & diarization
* 🧵 Display captions in spatial proximity to each speaker
* 🌌 Works with XREAL, Vuzix, or compatible AR glasses
* 🚀 Fully portable setup powered by Raspberry Pi + phone

---

## 👩‍💻 Architecture

```
Roger Table Mic
   ⬇️
Roger MyLink (3.5mm Output)
   ⬇️
USB Sound Card + Raspberry Pi Zero W
   ⬇️ Wi-Fi Audio Streaming
Smartphone
   ⬇️
[Whisper/Vosk ASR + CV Speaker Tracking]
   ⬇️
Caption Overlay Positioned by Face Detection
   ⬇️
AR Glasses (BLE or Wi-Fi)
```

---

## 🔧 Tech Stack

### Audio Input & Streaming

* **Roger Table Mic + MyLink**
* **Raspberry Pi Zero W** (Wi-Fi server)
* **PyAudio**, **FFmpeg**, or **GStreamer** for audio capture

### Transcription

* [ ] OpenAI **Whisper** (default, local)
* [ ] **Vosk** (offline)
* [ ] **Google Speech-to-Text** (cloud)

### Speaker Tracking

* **MediaPipe Face Mesh** or **YOLOv8** (face detection)
* **WhisperX** or **pyannote-audio** (diarization)

### Mobile App

* **Android SDK** (Kotlin/Java)
* **CameraX** + **MLKit** or OpenCV
* **Bluetooth/Wi-Fi** communication
* **Jetpack Compose** or Canvas for overlays

### AR Glasses

* Product TBD

---

## 📊 MVP Goals

* [ ] Real-time audio capture and Wi-Fi stream from Pi
* [ ] Mobile app to receive stream and transcribe
* [ ] Visual CV-based caption positioning
* [ ] Send overlays to AR glasses
* [ ] Diarization to distinguish speakers

---

## 🚀 How to Use

1. Power on your **Phonak Roger Table Mic** + **MyLink**
2. Connect MyLink → 3.5mm → USB Sound Card → OTG Adapter → **Raspberry Pi**
3. Launch the **Raspberry Pi Wi-Fi audio stream server**
4. Open **CaptionMe App** on smartphone
5. Connect to Pi stream, start live transcription
6. Connect **AR glasses** to receive caption overlay stream

---

## 💡 Future Enhancements

* Real-time **language translation**
* **3D face mesh** for more accurate overlay alignment
* Upload **captions to cloud** for extensible features and creative use

---

## 🤝 Contributing

PRs and community input are welcome! The goal is to build an inclusive, modular system that can be easily customized and expanded.

---

> CaptionMe bridges the physical and digital worlds — creating real-time, face-anchored, live subtitles to empower conversation and inclusion.
