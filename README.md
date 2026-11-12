# Securing Assistive Eye-Monitoring Technology

An **IoMT (Internet of Medical Things)** and **patient privacy**-focused eye-monitoring web prototype designed to assist individuals with severe motor impairments, such as paralysis and Amyotrophic Lateral Sclerosis (ALS). Built with client-side security controls, local visual privacy masking, and encrypted Firebase cloud synchronization.

## Live Demo
Access the deployed web application directly in your browser:  
**[Launch Live Prototype](https://cosmosfemme.github.io/securing-eye-monitor-accessibility-technology/)**

---

## Core Features
- **Real-Time Eye-Gaze Tracking:** Browser-based webcam stream processing with an HTML5 Canvas overlay for responsive, hands-free assistive control.
- **Patient Privacy & Visual Masking:** Local frame processing and facial privacy masking ensure raw patient video never leaves the client device unmasked.
- **End-to-End Data Security:** Client-side encryption and strict access controls safeguard gaze tracking metrics against unauthorized interception and cyberattacks.
- **IoMT Cloud Synchronization:** Real-time integration with Firebase for reliable patient state logging and secure remote caregiver monitoring.
- **Zero-Installation Access:** Hosted via GitHub Pages for instant cross-platform testing without local software dependencies.

---

## System Architecture & Tech Stack
- **Frontend & Local Processing:** HTML5, CSS3, JavaScript (ES6+), HTML5 Canvas API, WebRTC (`navigator.mediaDevices`)
- **Cloud & IoMT Backend:** Firebase (Realtime Database / Firestore)
- **Hosting & Deployment:** GitHub Pages

---

## How to Run & Test
1. Open the **[Live Demo Link](https://cosmosfemme.github.io/securing-eye-monitor-accessibility-technology/)**.
2. Grant browser **Camera permissions** when prompted to initialize the live eye-tracking feed.
3. Toggle privacy masking and cloud sync options within the interface to verify real-time biometric data streams and security controls.
