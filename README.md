# AI-driven EEG Communication Platform (CS/SSW 555, Team-6)

## Overview
This project delivers a cutting-edge **brain-computer interface (BCI)** web application aimed at enabling **real-time, non-verbal communication** for speech-impaired individuals. By leveraging EEG (electroencephalogram) signals to capture brain activity linked to imagined speech commands, the system uses a custom deep learning model to decode neural signals into actionable text commands, facilitating seamless communication between patients and doctors.


## Motivation

Speech impairments drastically limit individuals' ability to communicate, impacting their quality of life and independence. Traditional assistive technologies often rely on physical inputs, which may not be feasible for all users. This project aims to bridge that gap by developing a **non-invasive, AI-driven communication system** that translates brain signals directly into spoken or typed words, empowering users to interact naturally using their thoughts alone.

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
- **Backend Processing:** FastAPI backend receives EEG data streams, preprocesses signals, and passes them to the PyTorch model for classification.
- **Machine Learning Model:** The EEGAutoencoderClassifier processes EEG data in real-time, predicting multi-class speech commands such as “hello,” “help me,” and “stop.”
- **Frontend Interface:** Angular frontend provides an interactive UI for patients and doctors to communicate seamlessly, displaying live predictions and session data.
- **Data Management:** MongoDB securely stores EEG session logs, user profiles, and prediction results for auditing and improvement.
- **API Layer:** RESTful APIs facilitate communication between frontend and backend, ensuring scalability and maintainability.

## Usage

### Prerequisites
- Python 3.8+
- Node.js and Angular CLI
- MongoDB instance running locally or remotely
- EEG hardware setup compatible with the system

### Setup Backend
1. Clone the repository:
   ```bash
   git clone https://github.com/AradhanaRamamoorthy/EEG-Based-Predictive-Communication-System
   cd EEG-Based-Predictive-Communication-System/backend

To run the application,

go to backend -> open terminal -> run "npm start"
go to neucipher-frontend -> open terminal -> run "npm start"
go to model folder -> open terminal -> run "python server.py"


NOTE : You may require these dependencies to install :   pip install fastapi uvicorn pydantic

Please find all the required Jsons & .pt model here : https://drive.google.com/drive/u/1/folders/1u6sAHUsmFOJ8-OoI3KAqkGMXaVTUjthR

put these Jsons and folder in the model folder for a smooth run.



Find the video demonstration of our application here : https://drive.google.com/file/d/1iogjqR-12rYwTx82nbC9H1QV2d5VeJXp/view
