# Mental Predictor

`Mental_predictor` is a machine learning web app that predicts a student's `Mental_Health_Score` from lifestyle, study, screen-time, and stress-related inputs.

The project has two parts:

- A `FastAPI` backend in `main.py` that loads a saved scikit-learn pipeline and exposes a prediction endpoint.
- A static frontend (`index.html`, `script.js`, `style.css`) that collects user inputs and shows the predicted score in a dashboard UI.


## Run locally

### 1. Install dependencies

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

### 2. Start the backend

```powershell
uvicorn main:app --reload --port 2200
```

### 3. Open the frontend

Open `index.html` in a browser, or serve the folder with any simple static server.

Important: `script.js` currently points to this deployed API:

```js
const API_BASE = "https://mental-health-score-predictor-bqrc.onrender.com";
```

If you want the page to talk to your local FastAPI server instead, change it to:

```js
const API_BASE = "http://127.0.0.1:2200";
```


## Disclaimer

This project provides a predicted score for informational and educational use. It is not a medical or clinical diagnosis tool.
