# Final Project - Emotion Detector (OAQJP Emb AI)

This repository contains the **Final Project for the OAQJP Embedded AI course**.
The project implements a web-based **Emotion Detector** that analyzes user-provided text and identifies emotions.

The system supports two possible backends:

* **IBM Watson Natural Language Understanding** (used when credentials are configured)
* **Hugging Face Transformers** as a fallback model

## Project Overview

The Emotion Detector web application allows users to input text and receive an analysis of the emotional tone present in that text. The application is implemented as a lightweight web server.

## Running the Application Locally

1. Install the required dependencies:

```
pip install -r requirements.txt
```

2. Start the web server:

```
python server.py
```

3. Open your browser and go to:

```
http://localhost:5000
```

## Testing

Run the unit tests using:

```
python -m pytest -q
```

## Configuration

To enable **IBM Watson Natural Language Understanding**, set the following environment variables:

* `WATSON_APIKEY`
* `WATSON_URL`

If these variables are not set, the application will automatically use the **Hugging Face Transformers** backend.

## Notes

For deterministic testing, the project supports the following environment variable:

```
EMOTION_DETECTION_DRY_RUN=1
```

This ensures predictable outputs during automated tests.
