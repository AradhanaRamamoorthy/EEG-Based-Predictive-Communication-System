# AI-driven EEG Communication Platform (CS/SSW 555, Team-6)
*Enabling seamless thought-to-text communication for speech-impaired users through EEG and deep learning.*

## Overview
This project delivers a cutting-edge **brain-computer interface (BCI)** web application aimed at enabling **real-time, non-verbal communication** for speech-impaired individuals. By leveraging EEG (electroencephalogram) signals to capture brain activity linked to imagined speech commands, the system uses a custom deep learning model to decode neural signals into actionable text commands. These recognized commands are then streamed in real time to a dedicated doctor dashboard, facilitating seamless communication between patients and healthcare providers.
## Motivation

Speech impairment limits millions from expressing themselves, often isolating them socially and medically. Current assistive tech requires physical input, which is not always feasible. This project provides a **non-invasive, AI-powered solution** that translates thought into communication, empowering users with new freedom.

## Video Demonstration

*Watch this video for a quick walkthrough of the project in action.*
[Project Demo](https://drive.google.com/file/d/1iogjqR-12rYwTx82nbC9H1QV2d5VeJXp/view)

## Tech Stack & Tools

- **Frontend:** Angular — for building a responsive and intuitive user interface.
- **Backend:** FastAPI (Python) — serving RESTful APIs and handling real-time EEG data processing.
- **Database:** MongoDB — storing user data, EEG sessions, and prediction logs securely.
- **Machine Learning:** PyTorch — designing, training, and deploying the EEGAutoencoderClassifier model for signal classification.
- **Hardware Integration:** EEG devices — capturing raw neural signals related to imagined speech.
- **Development Practices:** Agile methodology and Test-Driven Development (TDD) — ensuring iterative improvements, code quality, and reliability.

## Project Architecture

The system is designed as a full-stack application integrating hardware, machine learning, and web technologies:

- **EEG Signal Acquisition:** EEG hardware captures raw neural signals representing imagined speech commands.
- **Backend Processing:** FastAPI backend receives EEG data streams and preprocesses signals.
- **Machine Learning Model:** EEGAutoencoderClassifier predicts multi-class speech commands in real time.
- **Frontend Interface:** Angular frontend includes a patient interface to capture EEG commands and a *doctor dashboard* that displays real-time decoded messages from each associated patient, enabling direct non-verbal communication.
- **Data Management:** MongoDB stores EEG session logs, user profiles, and prediction results.
- **API Layer:** RESTful APIs facilitate communication between frontend and backend.

## Prerequisites

Before setting up the project, ensure you have the following installed and configured on your machine:

- Python 3.8 or higher
- Node.js (latest LTS version recommended)
- Angular CLI (`npm install -g @angular/cli`)
- MongoDB (version 6.0 or later recommended)
---

> Run the following commands in your terminal or bash shell.
### Setup Backend
1. Clone the repository:
   ```bash
   git clone https://github.com/AradhanaRamamoorthy/EEG-Based-Predictive-Communication-System
   cd EEG-Based-Predictive-Communication-System/backend
   ```

2. Start the FastAPI
   ```bash
   uvicorn server:app --reload
   ```
   
### Setup Frontend
1. Navigate to the `Frontend` Directory:
   ```bash
   cd ../neucipher-frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run the Angular Application
   ```bash
   npm start
   ```
Open your browser at http://localhost:4200 to access the application.

### Backend dependencies for Model Inference
Install the following dependencies before running the model server:
```bash
pip install fastapi uvicorn pydantic
```

### Download Model and & JSON Files
Please download all the required .json files and the trained .pt model from the following Google Drive link:
[EEG Model Assets]( https://drive.google.com/drive/u/1/folders/1u6sAHUsmFOJ8-OoI3KAqkGMXaVTUjthR)

Place all downloaded files inside the `model/` directory to ensure the FastAPI model server runs smoothly.

### Model Deployment
1. Navigate to the `model` directory
   ```bash
   cd model
   ```
2. Start the backend Inference server
   ```bash
   python server.py
   ```
This launches the FastAPI server hosting the trained `EEGAutoencoderClassifier` model for real-time EEG signal prediction.

## Usage Example
1. **User dons EEG headset**, initiating brain signal capture.  
2. **Real-time EEG signals** are streamed securely to the backend server.  
3. The **PyTorch deep learning model processes EEG data**, predicting intended speech commands from neural activity.  
4. The **web frontend instantly displays recognized text commands** on the patient interface and transmits these messages to the **doctor dashboard**, allowing doctors to receive and respond to patient communications in real time.

## Key Features
- **Full-Stack Development:** Built with Angular frontend, FastAPI backend, and MongoDB storage, connected via RESTful APIs.  
- **EEG Signal Processing:** Integrated EEG hardware for real-time brain signal capture and classification.  
- **Deep Learning Model:** Trained and deployed a custom PyTorch EEGAutoencoderClassifier achieving ~70% accuracy.  
- **Real-Time Prediction:** Served model outputs using optimized FastAPI endpoints for low-latency response.  
- **Doctor Dashboard:** Real-time display of decoded EEG-based commands linked to individual patients for seamless clinical communication.
- **Agile & TDD:** Iterative development with Agile methodology and test-driven best practices.

## Impact & Benefits

- Enables communication for speech-impaired patients using brain signals.  
- Supports critical doctor-patient communication by providing doctors with real-time access to patients’ intended speech commands decoded from brain signals.
- Demonstrates real-world application of AI + BCI for assistive technology.  
- Paves the way for future advancements in neural interface systems.

## Future Directions
- Expand vocabulary for richer communication.  
- Reduce latency for faster real-time responses.  
- Integrate additional sensors like EMG and eye-tracking.  
- Collaborate with clinical partners for user trials and feedback.
