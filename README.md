# Junk-Mail-Jail
VITyarthi project for Fundamentals in AI and ML on Spam Email Classifier.

Project Title : Spam Email Classifier (Text Clssification)

Project Overview : The Junk Mail Jail project is a practical application of Natural Language Processing (NLP) and Machine Learning (ML) fundamentals, designed to automatically and accurately classify textual data. Developed for the Fundamentals in AI and ML course, the primary goal is to build an intelligent filter that identifies and separates unsolicited or harmful Spam messages from legitimate Ham messages.

This project goes beyond simple keyword matching by implementing a complete ML pipeline, demonstrating proficiency in the core stages of an ML workflow.

Features : The Junk Mail Jail project is a practical application of Natural Language Processing (NLP) and Machine Learning (ML) fundamentals, designed to automatically and accurately classify textual data. Developed for the Fundamentals in AI and ML course, the primary goal is to build an intelligent filter that identifies and separates unsolicited or harmful Spam messages from legitimate Ham messages.

This project goes beyond simple keyword matching by implementing a complete ML pipeline, demonstrating proficiency in the core stages of an ML workflow.

Technologies and Tools used :
1. Programming Language : Python 3.x
2. ML and NLP : Scikit Learn
3. Standard Python Libraries : os, io
4. Version Control : Git
5. Project Hosting : Github
6. Development Enviroment : Command Line Interface (CLI)

Steps to Install and Run the project :

Step 1: Clone the Repository
1. Open your terminal or command prompt.
2. Use the git clone command to download the project files.
3. Navigate into the newly created project directory.

Step 2: Setup Environment and Install Dependencies
This project relies on the pandas and scikit-learn libraries. Using a virtual environment is strongly recommended for managing dependencies.
1. Create a Virtual Environment.
2. Activate the VirtualEnvironment.
3. Install Required Librraries.

Step 3: Data Preparation
The script requires a CSV file named spam_data.csv to run the full training process.
1. Obtain the Data: Place your chosen spam/ham dataset (in CSV format) into the root of the Junk-Mail-Jail directory.
2. Ensure Formatting: Verify that the CSV contains the correct columns expected by the script (as configured in the load_data function in spam_classifier.py).

Step 4: Run the Application
1. Execute the main script from your activated virtual environment.
2. The script will automatically perform the ML workflow: load the data, preprocess the text, train the Multinomial Naive Bayes model, and display the evaluation metrics (Accuracy, Classification Report, and Confusion Matrix).

Steps  for Testing  : 

1. Envirnment and Data Verification
Test Case,Procedure,Expected Console Output
Data Loading,Run the script with spam_data.csv present and ensure the file is correctly loaded.,Confirmation message: Loading data from spam_data.csv...
Mock Data Fallback,Temporarily rename or remove spam_data.csv and run the script.,Confirmation message: Dataset file 'spam_data.csv' not found. Creating mock data.
Data Split,"After preprocessing, verify the size of the training and test sets. (Uses test_size=0.2).","Output confirming the split ratio, e.g., `Training set size: 6"

2. Model training and stability :
Test Case,Procedure,Expected Console Output
Training Execution,Run the script and observe the training phase.,Confirmation message: --- Training Model (Multinomial Naive Bayes) --- followed by Training complete.
Code Stability,"Introduce a known, non-fatal data format error (e.g., in a non-text column) and run the script.","The script should ideally handle the error gracefully (e.g., skip the row or cast safely) without crashing the entire ML pipeline."

3. Evaluation ad Prediction Verification
Test Case,Procedure,Expected Console Output/Metric Check
Accuracy Check,Observe the output of the evaluate_model function.,"Displays a numeric value for Accuracy, e.g., Accuracy: 0.9850."
Classification Report,"Verify the Precision, Recall, and F1-Score for both the 'Ham (0)' and 'Spam (1)' classes.","The metrics for the 'Ham' class should be high (near 1.0), as spam is typically less frequent but easier to miss."
Confusion Matrix Check,Verify the Confusion Matrix output: the top-left (True Negatives) and bottom-right (True Positives) values should be significantly higher than the off-diagonal values (False Positives/Negatives).,
Single Prediction (Spam),"Observe the test case with the obvious spam message: ""Congratulations! You have been selected to win a free iPhone!""",Predicted Label should be SPAM with high confidence.
Single Prediction (Ham),"Observe the test case with the legitimate message: ""Hey, can we meet for lunch tomorrow?""",Predicted Label should be HAM with high confidence.



