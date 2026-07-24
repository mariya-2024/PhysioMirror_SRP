# PhysioMirror_SRP
This is a socially relevant project that is build with the help of ai to improve physiotherapy. 

## Project Description

**PhysioMirror AI** is an AI-powered physiotherapy assistant that helps patients perform rehabilitation exercises correctly using real-time computer vision and pose estimation. The system analyzes body posture through a webcam, compares movements with clinically defined exercise blueprints, and provides instant visual and voice feedback to improve exercise accuracy.

The goal is to make physiotherapy sessions more accessible, reduce incorrect exercise execution at home, and assist physiotherapists by providing objective movement analysis and progress tracking.

---

# Problem Statement

Many patients perform physiotherapy exercises incorrectly when practicing at home due to the absence of continuous supervision. Incorrect posture can

* Slow recovery
* Increase pain
* Cause reinjury
* Reduce exercise effectiveness

Regular therapist appointments are also expensive and time-consuming.

PhysioMirror AI aims to bridge this gap through AI-assisted posture monitoring and real-time corrective feedback.

---

# Objectives

* Detect human body posture in real time using computer vision.
* Calculate joint angles for rehabilitation exercises.
* Compare patient posture against clinically approved movement templates.
* Provide instant visual and voice corrections.
* Count repetitions automatically.
* Track patient improvement across multiple sessions.
* Generate exercise reports for physiotherapists.

---

# Key Features

### Real-Time Pose Detection

Detects human body landmarks from webcam video using MediaPipe.

### Joint Angle Analysis

Calculates important joint angles such as

* Shoulder
* Elbow
* Hip
* Knee
* Ankle

to evaluate exercise form.

### Exercise Validation

Compares patient posture with predefined clinical exercise blueprints.

### Voice Feedback

Provides spoken guidance like

* Raise your arm higher
* Straighten your knee
* Slow down
* Hold for 5 seconds

using Text-to-Speech.

### Visual Feedback

* Green = Correct posture
* Yellow = Needs correction
* Red = Incorrect posture

Displays angle deviations directly on screen.

### Automatic Rep Counter

Counts repetitions only when the full movement is completed correctly.

### Progress Dashboard

Tracks

* Accuracy
* Repetitions
* Session duration
* Range of motion
* Weekly improvement

### Therapist Dashboard (Future)

Allows therapists to

* Review patient sessions
* Monitor progress
* Modify exercise plans
* Define tolerance thresholds

---

# Clinical Workflow

1. Therapist defines the exercise blueprint.
2. Patient starts webcam session.
3. Pose landmarks are detected.
4. Joint angles are calculated.
5. Angles are compared with exercise blueprint.
6. Real-time corrections are displayed.
7. Session statistics are stored.
8. Therapist reviews progress.

---

# System Architecture

```text
Webcam
   │
   ▼
MediaPipe Pose Detection
   │
   ▼
Joint Angle Calculator
   │
   ▼
Exercise Validation Engine
   │
   ▼
Feedback Engine
   │
   ├── Visual Overlay
   ├── Voice Feedback
   └── Rep Counter
   │
   ▼
Database
   │
   ▼
Dashboard
```

---

# Technology Stack

## Frontend

* React.js
* TypeScript
* Tailwind CSS
* HTML5
* CSS3
* Vite

---

## AI & Computer Vision

* MediaPipe Pose
* TensorFlow.js (if used for additional models)
* OpenCV.js (optional for preprocessing)

---

## Backend

* Node.js
* Express.js

---

## Database

* MongoDB
* Mongoose

---

## Authentication

* JWT Authentication
* bcrypt.js

---

## Voice Feedback

* Web Speech API
* Browser Text-to-Speech

---

## Charts & Dashboard

* Chart.js / Recharts

---

## Deployment

* Vercel (Frontend)
* Render / Railway (Backend)
* MongoDB Atlas

---

# Core Algorithms

* Pose Estimation
* Joint Angle Calculation
* Rule-Based Form Validation
* Exercise State Machine
* Repetition Detection
* Moving Average/Kalman Filter (for smoothing)
* Tolerance Threshold Analysis

---

# Folder Structure

```text
physiomirror-ai/

client/
    src/
        components/
        pages/
        hooks/
        utils/
        services/

server/
    controllers/
    routes/
    models/
    middleware/

shared/
    exercise_blueprints/

docs/
    architecture/
    diagrams/

README.md
```

---

# Future Enhancements

* Therapist Portal
* AI Exercise Recommendation
* Personalized Recovery Plans
* Multi-language Voice Feedback
* Pain Score Tracking
* Wearable Sensor Integration
* Teleconsultation
* Progress Prediction using Machine Learning

---

# Clinical Considerations

* Exercise blueprints are designed in consultation with physiotherapists.
* Tolerance thresholds are configurable.
* Real-time feedback supplements—not replaces—professional physiotherapy.
* User privacy is maintained by processing pose estimation locally whenever possible.

---

# Why This Project?

PhysioMirror AI combines Artificial Intelligence, Computer Vision, Healthcare, and Web Technologies to improve rehabilitation by providing affordable, accessible, and clinically guided exercise assistance.

---

# Tech Stack Summary

| Category       | Technology                               |
| -------------- | ---------------------------------------- |
| Frontend       | React.js, TypeScript, Tailwind CSS, Vite |
| Backend        | Node.js, Express.js                      |
| Database       | MongoDB Atlas, Mongoose                  |
| AI             | MediaPipe Pose, TensorFlow.js (optional) |
| Pose Analysis  | Joint Angle Calculation                  |
| Authentication | JWT, bcrypt                              |
| Voice Feedback | Web Speech API                           |
| Charts         | Chart.js / Recharts                      |
| Deployment     | Vercel, Render/Railway                   |

---

# Project Requirements

### Software

* Node.js (v18+)
* npm or Yarn
* MongoDB Atlas (or local MongoDB)
* Git
* VS Code

### Browser

* Chrome / Edge (latest version)
* Webcam access enabled

### Hardware

* Webcam (built-in or external)
* Internet connection
* Minimum 8 GB RAM recommended
* Dual-core processor or better

### Browser Permissions

* Camera access
* Microphone (optional, if voice interaction is added)
* Speaker/audio output for TTS feedback

---
