# Mental Health Score

## Project Overview

Mental Health Score is an educational machine-learning web application that estimates a student's mental health score using information about social media habits, academic activity, lifestyle, stress, and demographics. It demonstrates how a dataset can be used to develop a regression model and make its predictions available through an interactive web application.

The application returns an estimated score on a 0–10 scale. The result reflects patterns learned from the available data and should be treated as informational, not as a measure of an individual's overall well-being.

## Project Objectives

- Explore student survey data and prepare it for machine-learning analysis.
- Train and save a regression pipeline to estimate the target mental health score.
- Provide a Python API that validates input and obtains predictions from the saved model.
- Offer a browser-based form for entering student information and viewing results.
- Demonstrate the connection between data science, backend services, and frontend development.

## Data and Prediction Inputs

The included dataset contains 5,000 student records and 13 columns. The target column is `Mental_Health_Score`. The remaining columns describe student characteristics and reported habits:

- Age, gender, country, and academic level.
- Most-used social media platform and primary purpose of use.
- Average daily social media usage and daily phone unlocks.
- Study hours, physical activity hours, and sleep hours.
- Perceived stress level.

The API validates submitted values and uses the saved model pipeline to prepare the input and generate a prediction. Less common country values are grouped for model processing.

## How the Application Works

1. **Data analysis:** The notebook explores the student survey dataset and prepares features for model development.
2. **Model training:** A regression pipeline is trained to estimate the continuous mental health score. The trained pipeline is saved for reuse.
3. **Input collection:** The web page presents a form for entering the demographic, academic, social media, lifestyle, and stress information.
4. **Validation:** The browser checks form entries, and the Python API performs server-side validation before prediction.
5. **Prediction:** The API passes the submitted information to the saved pipeline and returns an estimated score.
6. **Result display:** The web page displays the score on a visual gauge and provides a descriptive result band, alongside helpful loading and error states.

## Technology

- **Machine learning and data processing:** Python, pandas, scikit-learn, and joblib.
- **Backend:** FastAPI, Pydantic, and Uvicorn.
- **Frontend:** HTML, CSS, and vanilla JavaScript.
- **Model development:** Jupyter Notebook.

## Project Structure

- `main.py` — Defines the FastAPI application, input validation, and prediction logic.
- `Mental_Health_Model.pkl` — Contains the saved model pipeline used by the API.
- `ML_Project.ipynb` — Documents model development and data analysis.
- `Student Social Media And Mental Health Impact.csv` — Supplies the student survey data.
- `index.html` — Defines the web form and prediction display.
- `style.css` — Provides the application's layout and visual styling.
- `script.js` — Handles browser-side validation, API communication, and result rendering.
- `requirements.txt` — Lists the Python packages required by the backend.
- `ML Project.html` — Provides an interactive project development and deployment blueprint.

## Responsible Use

This application is an educational demonstration, not a medical or clinical tool. Its prediction may be inaccurate and may not apply to a particular person. Do not use the result to diagnose, screen, or make decisions about anyone's health. Anyone concerned about their mental health should seek support from a qualified professional or a trusted person.
