# Final Project

## Watson NLP Emotion Detector

A Flask application that analyzes text with IBM Watson NLP and returns scores
for anger, disgust, fear, joy, and sadness, plus the dominant emotion.

### Setup

Use Python 3.10 or newer. From the project directory:

~~~bash
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt
~~~

On Windows PowerShell, activate with `.venv\Scripts\Activate.ps1`.

### Run the application

~~~bash
python3 server.py
~~~

Open http://127.0.0.1:5000. The API endpoint is
`/emotionDetector?textToAnalyze=your%20text`. Blank text returns HTTP 400;
Watson service or response errors return HTTP 502.

### Run unit tests

~~~bash
python3 -m unittest -v
~~~

The tests mock Watson so they do not need network access.

