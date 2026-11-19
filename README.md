# 🏋️ AI Gym Coach

### Your Personal AI-Powered Real-Time Fitness Trainer

[![Landing Page](https://img.shields.io/badge/Landing_Page-Live-00C853?style=for-the-badge&logo=netlify&logoColor=white)](https://aigymcoach77.netlify.app/)
[![Live Application](https://img.shields.io/badge/AI_Gym_Coach-Try_Now-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://gym-coachai.streamlit.app/)
[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-Framework-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io/)

**AI Gym Coach** is an intelligent, computer-vision-powered fitness application that transforms your webcam into a personal AI fitness trainer.

It uses real-time human pose estimation to analyze exercise movements, count repetitions, track workout progress, and provide AI-powered voice coaching feedback.

Whether you're performing squats, push-ups, or dumbbell exercises, AI Gym Coach helps you monitor your movements and improve your workout experience without requiring expensive fitness equipment.

---

## 🌐 Live Demo

Experience AI Gym Coach through the following links:

| Platform | Link |
|---|---|
| 🌍 Official Landing Page | [Visit Website](https://aigymcoach77.netlify.app/) |
| 🏋️ Live AI Application | [Launch Application](https://gym-coachai.streamlit.app/) |

### How to Use

1. Visit the official landing page.
2. Click on **Try it Live** to launch the application.
3. Log in to access the workout dashboard.
4. Select your exercise and configure sets and repetitions.
5. Allow camera permissions.
6. Position yourself in front of the camera.
7. Start your workout and experience real-time exercise tracking and coaching.

---

## ✨ Key Features

### 🎥 1. Real-Time Pose Detection
- Webcam-based exercise monitoring.
- Human body landmark detection using MediaPipe.
- Real-time movement and posture analysis.
- Visual pose tracking.

### 🔢 2. Automatic Rep & Set Counting
- Automatically counts exercise repetitions.
- Tracks completed sets.
- Monitors repetitions within the current set.
- Maintains workout progress in real time.

### 📐 3. Exercise Form Analysis
- Analyzes body movements and joint angles.
- Tracks exercise-specific movement patterns.
- Helps identify incorrect exercise positioning.
- Provides feedback to improve exercise technique.

### 🤖 4. AI-Powered Voice Coaching
- Integrates an LLM through the Groq API.
- Generates contextual workout feedback.
- Provides voice-based coaching using Google Text-to-Speech (gTTS).
- Helps users stay informed during workouts.

### 📊 5. Workout Tracking
- Tracks repetitions and sets.
- Maintains workout session metrics.
- Stores exercise information using SQLite.
- Provides a structured workout experience.

### 🔐 6. User Authentication
- Login interface.
- User-specific workout sessions.
- Persistent workout data storage.

### 🎨 7. Interactive User Interface
- Custom Streamlit dashboard.
- Dedicated landing page.
- Workout configuration controls.
- Real-time progress indicators.

---

## 🏋️ Supported Exercises

The application currently supports the following exercises:

| Exercise | Tracking |
|---|---|
| Squats | Rep counting and movement analysis |
| Push-ups | Rep counting and posture tracking |
| Biceps Curls (Dumbbell) | Arm movement and rep counting |
| Shoulder Press | Arm movement and rep tracking |
| Lunges | Lower-body movement tracking |

---

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Application Framework | Streamlit |
| Real-Time Video Streaming | Streamlit WebRTC |
| Computer Vision | OpenCV |
| Pose Estimation | MediaPipe Tasks |
| AI / LLM Integration | Groq API |
| Text-to-Speech | Google Text-to-Speech (gTTS) |
| Database | SQLite |
| Data Processing | NumPy, Pandas |
| Environment Management | python-dotenv |
| Landing Page Hosting | Netlify |
| Application Hosting | Streamlit Community Cloud |
| Version Control | Git & GitHub |

---

## 🧠 How It Works

AI Gym Coach combines computer vision, pose estimation, movement analysis, and generative AI to create an interactive fitness coaching experience.

### System Workflow

```text
             USER
               |
               v
         WEBCAM INPUT
               |
               v
      REAL-TIME VIDEO STREAM
               |
               v
       MEDIAPIPE POSE
          DETECTION
               |
               v
       BODY LANDMARK
         EXTRACTION
               |
               v
        JOINT ANGLE &
       MOVEMENT ANALYSIS
               |
               v
      EXERCISE-SPECIFIC
          DETECTION
               |
               v
       REP & SET COUNTING
               |
               v
        WORKOUT METRICS
               |
               v
         AI COACHING
          (GROQ API)
               |
               v
        TEXT-TO-SPEECH
            (gTTS)
               |
               v
       REAL-TIME VOICE
           FEEDBACK
```

### Technical Workflow

1. **Video Capture:** The webcam captures the user's exercise movements through real-time video streaming.
2. **Pose Estimation:** MediaPipe detects important human body landmarks.
3. **Landmark Extraction:** The system extracts coordinates of relevant body joints.
4. **Movement Analysis:** Joint angles and movement patterns are calculated.
5. **Exercise Detection:** Exercise-specific logic identifies movement states and repetitions.
6. **Workout Tracking:** Repetitions, sets, and workout metrics are updated.
7. **AI Coaching:** The Groq API generates contextual coaching feedback.
8. **Voice Feedback:** gTTS converts generated text into speech.
9. **Data Persistence:** SQLite stores relevant user and workout information.

---

## 🚀 Getting Started

Follow these steps to run AI Gym Coach locally.

### Prerequisites

Make sure you have:

- Python 3.10 or higher.
- Git installed.
- A working webcam.
- A modern web browser.
- A Groq API key for AI coaching functionality.

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

Navigate to the project directory:

```bash
cd YOUR_REPOSITORY
```

### 2. Navigate to the Main Application

Open the application directory containing `main.py` and `requirements.txt`.

### 3. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\activate
```

For Linux/macOS:

```bash
source .venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure Environment Variables

Create a `.env` file and configure your Groq API key:

```env
GROQ_API_KEY=your_groq_api_key
```

**Important:** Never upload your actual API keys or secret credentials to GitHub.

For deployed applications, configure secrets through the hosting platform.

### 6. Run the Application

```bash
streamlit run main.py
```

Open the local application:

```text
http://localhost:8501
```

Allow webcam permissions when prompted.

---

## 🔊 AI & Voice Coaching

The application integrates two technologies for interactive voice-based coaching.

### Groq API
- Generates AI-powered workout feedback.
- Provides contextual coaching responses.
- Supports intelligent interaction during workouts.

### Google Text-to-Speech (gTTS)
- Converts coaching messages into audio.
- Provides spoken feedback.
- Makes workout interaction more convenient.

---

## 🗄️ Database & Persistence

AI Gym Coach uses SQLite for lightweight data persistence.

The database layer is designed to manage:

- User information.
- Exercise records.
- Workout-related information.
- Session progress and tracking data.

SQLite provides a simple database solution without requiring a separate database server.

---

## 🌍 Deployment Architecture

The project uses separate hosting platforms for the landing page and the main application.

| Component | Platform | Link |
|---|---|---|
| Landing Page | Netlify | [Visit Website](https://aigymcoach77.netlify.app/) |
| Main AI Application | Streamlit Community Cloud | [Launch Application](https://gym-coachai.streamlit.app/) |
| Source Code | GitHub | Repository |

The landing page acts as the project's public-facing website, while the Streamlit application handles the AI-powered workout functionality.

---

## 🔒 Privacy & Security

- Camera access requires browser permission.
- API keys should be stored securely using environment variables or deployment secrets.
- Sensitive credentials should never be committed to version control.
- Users should ensure they have sufficient space and lighting for accurate pose detection.

---

## 🔮 Future Improvements

Some potential enhancements include:

- Personalized workout recommendations.
- More exercise detection algorithms.
- Advanced posture correction.
- Workout history and analytics dashboard.
- Calorie estimation.
- Exercise performance scoring.
- More advanced AI-based fitness recommendations.
- Mobile-friendly workout experience.

---

## 🎯 Project Objective

The primary objective of AI Gym Coach is to make intelligent fitness coaching more accessible by combining computer vision, artificial intelligence, and voice technology.

It demonstrates how real-time pose estimation and AI-driven feedback can be integrated into a practical application to improve the workout experience.

---

## 👨‍💻 Author

**Danish Khan**

Computer Science & Engineering | AI & ML Enthusiast | Developer

- GitHub: [Danish-khan77](https://github.com/Danish-khan77)
- LinkedIn: [Danish Khan](https://linkedin.com/in/danish-khan-cse)

---

## ⭐ Support

If you find this project interesting or useful, consider giving it a ⭐ on GitHub.

Your support and feedback are appreciated!

---

<p align="center">
  <b>AI Gym Coach — Your Form. Analyzed. Corrected. In Real Time.</b>
  <br/>
  Built with ❤️ using Python, Computer Vision and Generative AI.
</p>