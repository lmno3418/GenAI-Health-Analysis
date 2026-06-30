# Health Analysis App

A Streamlit app for analyzing blood work reports with Gemini via LangChain. The app lets you paste a blood report, extracts values, classifies them as high, low, or normal, and then generates a simple health summary plus an Indian diet plan.

## What It Does

- Accepts a pasted blood work report in plain text.
- Uses `langchain-google-genai` to call a Gemini model.
- Produces two outputs:
  - a short health summary
  - a practical Indian diet plan
- Displays both outputs in scrollable panels inside the app.

## Requirements

- Python 3.14 or later
- A Google API key stored locally in an `.env` file
- The packages listed in the root `requirements.txt`

The app reads the API key from the environment variable `googleapikey`.

## Setup

1. Create and activate a virtual environment.
2. Install the dependencies from the project root:

   ```bash
   pip install -r requirements.txt
   ```

3. Create a local `.env` file in the project root with your API key:

   ```env
   googleapikey=your_google_api_key_here
   ```

## Run The App

From the `health_analysis` folder, start Streamlit:

```bash
streamlit run app.py
```

## How To Use

1. Paste your blood work report into the text area.
2. Click **Analyze**.
3. Review the extracted blood work values, health summary, and diet plan.

## Notes

- The model is currently set to `gemma-4-31b-it` in `app.py`.
- The app does not require uploaded files; it works directly from pasted text.
- `blood_work.txt` can be used as a sample input file if you want to test the flow quickly.
- `healthanalysis.ipynb` appears to be a notebook companion for experimentation, but the Streamlit app is the main entry point.

## Screenshots

### UI Preview

![Screenshot UI](/Screenshot-UI.png)

### Workflow Architecture

![Workflow Architecture](/workflow_architecture.png)
