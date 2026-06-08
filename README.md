# Conversation Safety Analyzer

An AI-powered NLP backend that detects emotional tone and potential manipulation patterns in text conversations using HuggingFace transformers and Flask.

## Features

* Emotion detection using BERT
* Manipulation pattern classification
* Safe response suggestion generation
* REST API backend
* Render deployment support

## Tech Stack

* Python
* Flask
* HuggingFace Transformers
* BERT
* Render

## API Endpoint

POST `/analyze`

Example request:

```json
{
  "message": "If you cared about me, you'd do this."
}
```

Example response:

```json
{
  "emotion": "sadness",
  "confidence": 91,
  "manipulation_type": "guilt",
  "safe_reply": "I’m not comfortable with this conversation right now.",
  "risk_score": 80
}
```

## How It Works

1. User message is sent to the Flask API.
2. HuggingFace BERT model predicts emotional tone.
3. Backend maps emotions to manipulation categories.
4. A safer conversational response is generated.

## Future Improvements

* Multi-label manipulation detection
* Context-aware conversation analysis
* Frontend integration
* Real-time chat monitoring
