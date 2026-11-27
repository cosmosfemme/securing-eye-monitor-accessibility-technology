# Securing Assistive Eye-Monitoring Technology

An **IoMT (Internet of Medical Things)** and **patient privacy**-focused eye-monitoring web prototype designed to assist individuals with severe motor impairments, such as paralysis and Amyotrophic Lateral Sclerosis (ALS). Built with client-side security controls, local visual privacy masking, and encrypted Firebase cloud synchronization.

> **Disclaimer:** The work is an academic proof of concept, **not** a clinically certified medical device,and should not be used for clinical diagnosis, treatment, or life-critical monitoring . It shows that practical assistive eye monitoring and remote status synchronisation can be achieved while putting patient confidentiality, accessible usability and defense-in-depth security first. 

## Live Demo
Access the deployed web application directly in your browser:  
**[Launch Live Prototype](https://cosmosfemme.github.io/securing-eye-monitor-accessibility-technology/)**

---

## Core Features
- **Local Eye/Iris Landmark Detection:** MediaPipe Face Mesh detects face and iris landmarks in the browser and displays an approximate eye-direction estimate. It is not calibrated screen gaze or a medical measurement.
- **Patient Privacy & Visual Masking:** The live camera preview is pixelated across the full frame in the browser. Captured frames use the masked preview; raw video is not saved or sent to Firebase.
- **End-to-End Data Security:** Client-side encryption and strict access controls safeguard gaze tracking metrics against unauthorized interception and cyberattacks.
- **IoMT Cloud Synchronization:** Encrypted patient messages, status flags, and simulation events can be synced to Firebase under an anonymous user's UID. Realtime Database rules must enforce per-user access; video and gaze coordinates remain local.
- **Zero-Installation Access:** Hosted via GitHub Pages for instant cross-platform testing without local software dependencies.

---

## System Architecture & Tech Stack
- **Frontend & Local Processing:** HTML5, CSS3, JavaScript (ES6+), MediaPipe Face Mesh, HTML5 Canvas API, WebRTC (`navigator.mediaDevices`)
- **Cloud & IoMT Backend:** Firebase (Realtime Database / Firestore)
- **Hosting & Deployment:** GitHub Pages

---

## How to Run & Test
1. Open the **[Live Demo Link](https://cosmosfemme.github.io/securing-eye-monitor-accessibility-technology/)**.
2. Grant browser **Camera permissions** when prompted. Allow the MediaPipe Face Mesh library and model files to load; face and iris landmark inference runs locally in the browser.
3. Enable the camera to view the pixelated preview, then capture a masked frame. The raw video is not saved or uploaded.
4. Enter a passphrase and choose **Encrypt & Sync Status Flags** to send encrypted status flags and timestamps to Firebase.
5. Enable Anonymous sign-in in Firebase Authentication and configure Realtime Database rules for `/users/{uid}/secure_gaze_logs/{recordId}` before syncing records.
