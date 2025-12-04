Cardiovascular Risk Integrated Support Platform
CBB7400 — Final Project Code Repository

Project Description

This repository contains the full implementation of our cardiovascular risk prediction system and Clinical Decision Support (CDS) prototype. Using the publicly available Framingham Heart Study dataset, we developed a reduced logistic regression model that predicts the 10-year risk of coronary heart disease (CHD).

Our workflow includes:
- exploratory data analysis
- handling missingness and class imbalance
- model training and evaluation
- significance based variable reduction
- threshold analysis
- odds ratio interpretation
- deployment of the reduced model in an interactive Streamlit application

The CDS application transforms model output into clinically meaningful risk categories (low / moderate / high), provides action-oriented suggestions, and reflects principles of human-centered CDS design, such as low cognitive load, constrained input ranges, and visual risk presentation.


Application Files: 

Final_AppModel.py  - Streamlit application using the reduced logistic regression model, including warnings, risk categories, visual bars, and downloadable summaries. (using the logreg_model_reduced.pkl-)
Reduced_App.py- Earlier version of the app using the reduced model (kept for reference). ( using the logreg_model_reduced.pkl)
Itinial_App.py - First app made with all the variable no selection of variables have occured yet ( using the logreg_model.pkl)

Model Files:

logreg_model.pkl- Full logistic regression model (before reduction).
logreg_model_reduced.pkl- Final reduced logistic regression model used in our CDS tool.

Notebook:

DataSet_Coding.ipynb- Complete workflow: preprocessing, model training, evaluation, threshold analysis, and odds ratio extraction.

Environment:

requirements.txt- Python dependencies required to run the Streamlit app and load models.



How to Run the Application:
1. Install required dependencies
   - Make sure you are in your project environment, then run:     pip install -r requirements.txt

2. Launch the Streamlit CDS tool
   - streamlit run Final_AppModel.py

4. Use the Application
   - Enter patient demographic + clinical values
   - View predicted 10-year CHD probability
   - See assigned risk category (low / moderate / high)
   - Read the brief clinical recommendation
   - Review warnings for implausible input values
   - Download a risk summary for documentation

