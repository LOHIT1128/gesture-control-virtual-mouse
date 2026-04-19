# 🖱️ Gesture Controlled Virtual Mouse

> A hands-free, AI-powered virtual mouse system that uses real-time hand gesture recognition to control your computer — and even solve math problems using drawn equations.

---

## 📌 Project Overview

This project was developed as part of a **B.Tech in Information Technology** at **MVGR College of Engineering (A), Vizianagaram**, during the academic year 2024–25.

The system uses a webcam and computer vision libraries to detect hand gestures in real time, translating them into mouse actions like moving, clicking, dragging, and drawing — with no physical hardware required. It also integrates **Google's Generative AI (Gemini)** to solve handwritten math equations drawn by the user via gesture.

---

## 👨‍💻 Team

| Name | 
|------|------------|

| Perisetty Sai Lohit |



---

## ✨ Features

- **Hand Gesture-Based Mouse Control** — Move the cursor, left-click, right-click, and drag using hand gestures tracked via MediaPipe
- **AI-Powered Math Solver** — Draw math equations on screen and send them to Google Gemini AI for instant solutions
- **Real-Time Hand Tracking** — 21 hand landmarks detected per frame using MediaPipe
- **Gesture Smoothing** — Smoothening algorithms ensure stable, jitter-free cursor movement
- **Streamlit UI** — Webcam feed and AI results displayed in a clean web interface

---

## 🤝 Gesture Mapping

| Gesture | Action |
|---------|--------|
| Index finger raised | Move mouse cursor |
| All fingers raised | Left click |
| Index + middle fingers raised | Right click |
| Thumb raised | Drag (click and hold) |
| Index finger raised (in draw mode) | Draw on canvas |
| Index + middle fingers raised (in draw mode) | Idle / pause drawing |
| All fingers except little finger raised | Submit drawing to AI |
| All fingers raised (in draw mode) | Clear canvas |

---

## 🛠️ Tech Stack

| Category | Tools / Libraries |
|----------|-----------------|
| Language | Python 3.10 |
| Hand Tracking | MediaPipe |
| Computer Vision | OpenCV |
| Mouse Automation | AutoPy, PyAutoGUI |
| Math Calculations | NumPy |
| Image Processing | Pillow (PIL) |
| UI | Streamlit |
| AI Integration | Google Generative AI (Gemini 1.5 Flash) |
| IDE | PyCharm |

---

## 💻 Hardware Requirements

- Processor: Intel i3 or higher
- RAM: 4 GB minimum
- Hard Disk: 500 GB
- Webcam (built-in or external)

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/gesture-controlled-virtual-mouse.git
cd gesture-controlled-virtual-mouse
```

### 2. Install dependencies

```bash
pip install opencv-python mediapipe autopy pyautogui numpy pillow streamlit google-generativeai cvzone
```

> **Note:** `autopy` may require additional setup on some systems. On Linux, install `libxtst-dev` and `python3-dev` before installing autopy.

### 3. Add your Google Gemini API key

Open `GeastureandMath.py` and replace the API key:

```python
genai.configure(api_key="YOUR_GEMINI_API_KEY")
```

Get a free API key at [https://aistudio.google.com](https://aistudio.google.com)

---

## 🚀 Usage

### Run the Virtual Mouse

```bash
python VirtualMouse.py
```

A webcam window will open. Use your hand gestures in front of the camera to control the mouse.

### Run the Gesture + Math Solver (Streamlit App)

```bash
streamlit run GeastureandMath.py
```

Open the browser tab that appears (usually `http://localhost:8501`). Use the index finger to draw a math equation, then raise all fingers except the little finger to submit it to the AI.

---

## 📁 Project Structure

```
gesture-controlled-virtual-mouse/
│
├── HandTrackingModule.py      # Core hand detection and tracking logic
├── VirtualMouse.py            # Virtual mouse control via gestures
├── GeastureandMath.py         # Streamlit app: gesture drawing + AI math solver
├── Mathdraw.png               # Banner image for Streamlit UI
└── README.md
```

---

## 🧠 How It Works

1. **Webcam captures frames** in real time
2. **MediaPipe** detects 21 hand landmarks per frame
3. **Finger states** (up/down) are determined by comparing landmark positions
4. **Gesture is mapped** to a system action (move, click, draw, submit)
5. For math solving: the drawn canvas is sent as an image to **Google Gemini AI**, which returns the solution
6. The solution is displayed live in the **Streamlit interface**

---

## 📊 Performance

| Metric | Result |
|--------|--------|
| Gesture recognition accuracy | ~95% |
| Response latency | Real-time (minimal delay) |
| Supported lighting conditions | Normal to slightly dim (bright light can cause issues) |
| Platform support | Windows, macOS, Linux |

---

## ⚠️ Known Limitations

- Excessive brightness may affect gesture detection accuracy
- Overlapping or occluded fingers can reduce recognition precision
- Complex gestures performed simultaneously may introduce slight delays
- Reflective or cluttered backgrounds may interfere with hand tracking

---

## 🔮 Future Enhancements

- Support for more complex gestures (scrolling, zooming, multi-finger pinch)
- Machine learning personalization to adapt to individual users' hand movements
- Voice recognition integration for hybrid input
- Cross-platform compatibility with smartphones and tablets
- VR/AR environment integration

---

## 📚 References

1. S. Mitra and T. Acharya. *Gesture Recognition: A Survey*. IEEE Transactions on Systems, Man, and Cybernetics, Vol. 37(3), 2007.
2. Abhik Banerjee et al. *Mouse Control using a Web Camera based on Colour Detection*.
3. Jayashree Katti et al. *Home Automation Techniques Based on Hand Gesture Recognition*.
4. Nasser H. Dardas, Mohammad Alhaj. *Hand Gesture Interaction with a 3D Virtual Environment*. Research Bulletin of Jordan ACM, Vol. II(III).
5. Mahalakshmi S, S. Nirmal, Dr. L. Suriya Kala. *Eye Controlled Mouse Cursor*. IEEE ICCV, June 2023.

---

## 📄 License

This project was developed for academic purposes at MVGR College of Engineering (A), Vizianagaram, affiliated to JNTU Kakinada. Free to use for educational and non-commercial purposes.
