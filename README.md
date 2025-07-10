# 🧍‍♂️ Full-Stack Rule-Based Bad Posture Detection App

This project is a full-stack web application that detects bad posture from a user-uploaded video or webcam input. It uses MediaPipe and OpenCV to extract body keypoints and applies rule-based logic to identify poor postural positions (e.g., slouching, knees over toes, hunched back, etc.).

---

## 🛠 Tech Stack

### Frontend:
- **React.js**
- **Axios** (for API requests)
- **react-webcam** (for capturing webcam frames)

### Backend:
- **FastAPI**
- **MediaPipe** (pose estimation)
- **OpenCV**
- **NumPy**
- **Uvicorn** (ASGI server)

---

## 🚀 Features

- Upload video or use webcam to record posture
- Detect bad posture using three rules:
  - **Back angle < 150°**
  - **Knee goes beyond toe**
  - **Neck bend > 30°**
- Real-time or frame-by-frame feedback
- Annotated output video with posture markings
- Downloadable video with alerts
- Deployed frontend and backend

---

## 📸 Demo

▶️ **Demo Video**: [Watch here](https://drive.google.com/file/d/your_demo_video_link_here/view)

---

## 🌐 Live Links

- 🔗 **Frontend (React)**: [https://your-frontend-url.netlify.app](https://your-frontend-url.netlify.app)
- 🔗 **Backend (FastAPI)**: [https://your-backend-url.onrender.com](https://your-backend-url.onrender.com)

---

## 🧪 How to Run Locally

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/posture-detector.git
cd posture-detector
