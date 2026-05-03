# DEEP LEARNING

## Run the Streamlit App (Windows)

### Prerequisites

- Miniconda or Anaconda installed
- Model file present at `streamlit/cnn_classifier.h5`

### 1) Go to the project folder

```powershell
cd C:\...\CCDEPLRL_PROJECT
```

### 2) Create a compatible environment (Python 3.11)

TensorFlow and NumPy in this project are compatible with Python 3.11.

```powershell
conda create -n ccdeplrl_py311 python=3.11 -y
```

### 3) Activate the environment

```powershell
conda activate ccdeplrl_py311
```

### 4) Install dependencies

```powershell
pip install --upgrade pip
pip install -r .\streamlit\requirements.txt
```

### 5) Run the app

```powershell
streamlit run .\streamlit\app.py
```

Then open: `http://localhost:8501`

## One-line run (without activating env)

```powershell
conda run -n ccdeplrl_py311 streamlit run .\streamlit\app.py
```

## Notes

- Keep the model file at `streamlit/cnn_classifier.h5` (same folder as `streamlit/app.py`).
- If you run from a fresh machine, repeat steps 2 to 4 once.
- Requirements file is in `streamlit/requirements.txt`.

## Common issue

If installation fails while building NumPy from source, you are likely using Python 3.13. Use Python 3.11 as shown above.