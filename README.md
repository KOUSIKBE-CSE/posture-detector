# 🧍‍♂️ Full-Stack Rule-Based Bad Posture Detection App

A full-stack AI-powered application that detects **bad posture** during **squats** or **desk sitting** using **rule-based logic** and **pose estimation**.
The system uses MediaPipe Pose to track 33 body landmarks and applies geometric rules to evaluate posture in real time.

---

## 📌 Problem Statement

Poor posture during workouts or prolonged desk work can cause injuries or long-term health problems.
While many solutions rely on heavy machine learning models, this project demonstrates a **lightweight, rule-based alternative** that works efficiently in the browser with minimal latency.

---

## 🛠️ Tech Stack Overview

**Frontend:**

* React.js (Vite) for building a fast, responsive UI
* Tailwind CSS for modern styling
* React Webcam for live camera input
* Axios for communication with the backend

**Backend:**

* FastAPI (Python) for building APIs
* OpenCV for video frame processing
* MediaPipe Pose for landmark detection

**Deployment:**

* Netlify for hosting the frontend
* Render for hosting the backend
* FastAPI static routes for serving processed videos

---

## ⚙️ How It Works

1. **Video Input** – The user uploads a video or streams their webcam feed.
2. **Pose Detection** – MediaPipe Pose identifies 33 body landmarks in each frame.
3. **Rule-Based Checks** –

   * **Neck Bend:** Angle greater than 30° triggers a warning.
   * **Back Posture:** A non-straight back triggers a “slouch” alert.
   * **Knee Position (Squats):** If the knee moves beyond the toe, a form warning is shown.
4. **Annotated Feedback** – The backend processes the video and returns an annotated version with posture alerts.
5. **Posture Score** – An overall score is displayed to help users track improvement.

---

## 📜 Algorithm Explanation

The posture detection logic follows a **geometric, rule-based approach**:

1. **Landmark Extraction**

   * MediaPipe provides `(x, y, z)` coordinates for 33 key points on the human body.
   * These include shoulders, hips, knees, ankles, and head points.

2. **Angle Calculation**

   * We calculate angles between three connected landmarks using vector math.
   * Example: Neck bend is measured as the angle between the **shoulder–neck–ear** points.

3. **Threshold Rules**

   * For desk posture:

     * **Neck Bend Rule:** If the neck angle exceeds 30°, flag as “bent neck”.
     * **Back Straightness Rule:** If the back angle deviates from vertical by more than 15°, flag as “slouch”.
   * For squats:

     * **Knee Rule:** If the horizontal position of the knee passes beyond the toe, flag as “knee over toe”.

4. **Annotation & Feedback**

   * OpenCV draws visual cues such as lines, angles, and warning text on each frame.
   * Frames are recompiled into a processed video for playback.

5. **Score Calculation**

   * The score starts at 100 and deductions are applied for each detected posture violation.
   * The final score is displayed with qualitative feedback (e.g., “Excellent”, “Needs Improvement”).

This rule-based method ensures **fast, explainable, and lightweight posture evaluation** compared to heavy neural network inference.

---

## 🚀 Live Demo

**Frontend:** [https://your-netlify-site.netlify.app](https://your-netlify-site.netlify.app)
**Backend:** [https://your-backend.onrender.com](https://your-backend.onrender.com)

---

## 🎥 Demo Video

▶️ [Watch the demo](https://www.loom.com/share/10cc11cbcc8e42e58dce91290852be35?sid=8ec560df-17fc-496e-8c66-7116e728b9b9)

---

## 🧑‍💻 Local Setup

### Backend Setup

```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

---

## 📷 Screenshots

* **Upload & Analysis Screen** – Users can upload a video or start live webcam analysis.
* **Posture Score Display** – Shows the calculated score and posture feedback.
* **Annotated Video Output** – Highlights posture issues directly on the video.

---

## 🧩 Key Takeaways

* Demonstrates how AI landmark detection can be combined with simple rule-based logic.
* Offers a lightweight alternative to heavy ML models for posture tracking.
* Fully deployable as a web app accessible on any modern browser.

---
