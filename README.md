# AI-Based Detection of Nuanced Cyberbullying

### Smart Social Media Threat Detection System

## Overview

This project is an AI-powered cyber safety platform built to detect harmful online behavior across social media platforms like WhatsApp, Instagram, and Twitter. The system focuses on identifying nuanced cyberbullying, sarcasm-based toxicity, scams, fake media, phishing attempts, and online harassment.

The goal of the project is not just to classify toxic text, but to understand the intent and severity of harmful content and automatically decide the appropriate action such as monitoring, flagging, blocking, or reporting to a Cyber Hub.

The project was developed using Flask and Hugging Face Transformers with a Gen-Z-friendly interface and real-time simulated social media monitoring.

---

# Features

## Toxicity Detection

* Detects toxic and harmful language using the `unitary/toxic-bert` model.
* Classifies messages into:

  * Safe
  * Sarcastic
  * Risky
  * Toxic
  * Ultra Toxic

---

## Sarcasm Detection

The system checks for:

* sarcastic keywords
* emojis
* passive-aggressive tone

This helps identify cyberbullying that may not contain direct abusive words.

---

## Scam & Fraud Detection

Detects:

* phishing links
* fake giveaways
* OTP scams
* investment scams
* impersonation attempts
* suspicious financial requests

---

## Fake Media Detection

Identifies indicators of:

* deepfakes
* manipulated videos
* AI-generated media
* misinformation
* fake news content

---

## AI Auto-Action Engine

Based on threat severity, the system automatically:

* monitors content
* flags risky messages
* blocks dangerous content
* reports severe threats to Cyber Hub

---

## Mental Health Support

If highly toxic content is detected, the platform displays supportive mental health messages and helpline suggestions.

---

## Positive Rewrite Suggestions

The project can convert toxic text into a more respectful and constructive version using AI-generated polite rewrites.

---

## Simulated Social Media Feed

Includes simulated datasets for:

* WhatsApp
* Instagram
* Twitter

The platform scans these feeds and analyzes every post in real time.

---

# Tech Stack

## Backend

* Python
* Flask

## AI / ML

* Hugging Face Transformers
* Toxic-BERT (`unitary/toxic-bert`)
* NumPy

## Frontend

* HTML
* CSS
* JavaScript

---

# Project Structure

```text
project-folder/
│
├── templates/
│   └── index.html
│
├── static/
│   ├── style.css
│   ├── script.js
│
├── bully_detector.py
├── requirements.txt
└── README.md
```

---

# Installation

## 1. Clone Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

---

## 2. Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux / Mac

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Running the Project

```bash
python bully_detector.py
```

Server will start on:

```text
http://127.0.0.1:5000
```

---

# API Endpoints

## Analyze Text

### POST `/analyze`

Checks toxicity and sarcasm.

Example Request:

```json
{
  "text": "You're so useless"
}
```

---

## Scan Platform Feed

### POST `/api/platform/scan`

Example:

```json
{
  "platform": "whatsapp"
}
```

Supported platforms:

* whatsapp
* instagram
* twitter
* all

---

## Platform Statistics

### GET `/api/platform/stats`

Returns:

* threats detected
* blocked content
* reported cases
* platform statistics

---

## Cyber Hub Reports

### GET `/api/cyberhub/reports`

Shows all auto-generated reports.

---

# Detection Logic

The system combines:

* Toxicity score
* Sarcasm score
* Fraud indicators
* Fake media indicators

to generate an overall risk level.

A weighted scoring mechanism determines:

* severity
* threat category
* automatic action

---

# Auto Actions

| Severity | Action              |
| -------- | ------------------- |
| Low      | Monitor             |
| Medium   | Flag                |
| High     | Block               |
| Critical | Report to Cyber Hub |

---

# Error Handling & Debugging

During development, multiple debugging scripts were used to test:

* JSON serialization
* Flask API responses
* platform scan endpoints
* response formatting
* internal server errors

The project also includes a fallback SAFE MODE in case the AI model fails to load.

---

# Future Improvements

* Real social media API integration
* Real-time screenshot analysis
* Voice toxicity detection
* Multilingual cyberbullying detection
* User authentication system
* Database integration
* Admin dashboard
* Live moderation system

---

# Why This Project Matters

Cyberbullying today is no longer limited to direct abusive words. Many harmful interactions happen through sarcasm, manipulation, fake media, scams, and emotional targeting.

This project aims to create a smarter AI-based moderation system that understands online behavior more deeply and helps build safer digital communities.

---

# Team Vision

The vision behind this project is to combine:

* AI moderation
* online safety
* empathy
* mental health awareness

into one unified platform that not only detects harmful content but also encourages healthier online interactions.

---

# Author

# Prapti Sinha

Developed as a cybersecurity and AI innovation project focused on social media safety and nuanced cyberbullying detection.
