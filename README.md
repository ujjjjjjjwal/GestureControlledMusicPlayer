# 🎹 Gesture-Controlled Virtual Musical Instrument

A real-time **gesture-controlled virtual musical instrument** that allows users to play **piano and drums using only hand gestures and a webcam**.

This system uses **MediaPipe for hand tracking**, **OpenCV for video processing**, **Pygame for audio playback**, and **Streamlit for the UI**. Each hand gesture is encoded into a **5-bit binary representation**, enabling up to **32 unique gesture inputs**.


## 🚀 Features

* 🎥 Real-time hand gesture recognition using webcam
* 🖐️ 5-bit binary finger encoding (32 gesture combinations)
* 🎹 Piano and 🥁 Drum modes
* 🔄 Custom gesture-to-sound mapping
* 📄 Downloadable cheat sheets
* 🔊 Multi-channel audio playback (overlapping sounds)
* 🌐 Streamlit-based interactive UI
* 💻 No special hardware required (low-cost setup)

---

## 🧠 How It Works

1. Webcam captures live feed
2. MediaPipe detects hand landmarks
3. Finger states → binary encoding
4. Binary gesture → mapped to sound
5. Pygame plays sound
6. Streamlit UI manages interaction

---

## 🛠️ Tech Stack

* Python
* Streamlit
* MediaPipe
* OpenCV
* Pygame
* NumPy
* Pillow
* JSON

---

## 📁 Project Structure

```
GestureControlledMusicPlayer/
│
├── musicplayer.py
├── key_mapping.json
├── drum_cheat_sheet.txt
├── piano_cheat_sheet.txt
├── images/
├── sounds/
└── README.md
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone <YOUR_REPO_LINK_HERE>
cd GestureControlledMusicPlayer
```

Install dependencies:

```bash
pip install streamlit opencv-python mediapipe==0.10.8 pygame pillow numpy
```

---

## ▶️ Run the App

```bash
python -m streamlit run musicplayer.py
```

Then open:

```
http://localhost:8501
```

---

## ⚠️ Important: Update Hardcoded Paths

Before running the project, update the following lines in `musicplayer.py`:

* **Line ~304** → Gesture image folder
* **Line ~367** → Piano sound path
* **Line ~371** → Drum sound path
* **Line ~456–457** → Instrument icon paths

Replace:

```
C:/Users/hp/Desktop/GestureControlledMusicPlayer/
```

With:

```
images/
sounds/
```

### Example Fix

```python
IMAGE_FOLDER = "images/Hand-images/"
new_sound_path = f"sounds/Piano/key{key_number:02}.ogg"
new_sound_path = f"sounds/Drums/drum{key_number:02}.mp3"
```

💡 Tip: Converting to relative paths makes the project portable across systems.

---

## 🎮 Usage

* Launch the app
* Select instrument (Piano / Drums)
* Click **PLAY**
* Use hand gestures to trigger sounds
* Customize gesture mappings
* Download cheat sheets

---

## 📄 Research Paper

This project is based on:

**"Real-Time Gesture Recognition for Virtual Musical Instrument Control Using Binary Finger Encoding"**

```
https://www.ijfmr.com/research-paper.php?id=66600
```

## 🏆 Achievements / Highlights

* 🧠 Real-time gesture recognition system
* 🎵 Fully playable musical interface
* ⚡ Low-latency audio response
* 💡 Low-cost alternative to hardware instruments

## 🤝 Acknowledgments

* MediaPipe (Google)
* Streamlit
* OpenCV
* Pygame

---

## 👤 Author

Ujjwal Singh 
www.linkedin.com/in/ujjwal-uic

---
