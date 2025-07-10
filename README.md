# 🧍‍♂️ Full-Stack Rule-Based Bad Posture Detection App

A web application that detects **bad posture** during **squats** or **desk sitting** using **rule-based logic** and **pose estimation** with MediaPipe. Users can upload a video or use their webcam to receive real-time posture feedback.

---

## 🛠️ Tech Stack Used

### 👨‍💻 Frontend
- React.js (Vite)
- Tailwind CSS (UI Styling)
- Axios (API communication)
- React Webcam (for webcam capture)

### 🔧 Backend
- FastAPI (Python)
- OpenCV (video processing)
- MediaPipe (pose landmark detection)
- Uvicorn (server)

### ☁️ Deployment
- **Frontend**: Netlify  
- **Backend**: Render  
- **Video Hosting**: FastAPI static route (`/video/{filename}`)

---

## 🚀 Live Demo Links

- 🔗 **Frontend URL**: [https://your-netlify-site.netlify.app](https://your-netlify-site.netlify.app)
- 🔗 **Backend URL**: [https://your-backend.onrender.com](https://your-backend.onrender.com)

---

## 🎥 Demo Video

▶️ **Watch the demo:** https://www.loom.com/share/10cc11cbcc8e42e58dce91290852be35?sid=8ec560df-17fc-496e-8c66-7116e728b9b9

This video demonstrates:
- Uploading and analyzing a squat/desk video
- Real-time posture issue detection
- Annotated feedback display
- Code and logic explanation

---

## 🧑‍💻 How to Run Locally

### 📦 Prerequisites
- Node.js & npm
- Python 3.9+
- FFmpeg (for video encoding)
- pip / virtualenv

### 🔹 Backend Setup

```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload --host 0.0.0.0 --port 8000
