# Capstone: Artificial Intelligence & Machine Learning
Professional Certificate
Haas School of Business
University of California, Berkeley
<hr>

<img align="center" src="https://www.signitysolutions.com/blog/wp-content/uploads/2020/09/artificial-intelligence-in-healthcare-sector.jpg">
<b>Overview:</b> In this capstone, my goal is to do the heavy lifting of the project. I will explore my data source, testa a few of the techniqueues, and com up with a solution or answer to my research problem. HTML version of notebook is <a href="https://federalcomputing.com/capstoneAIML.html" parent="_blank">available here. </a>



<h3>Research Problem</h3>

Hospitals are slammed with readmissions of patients. Specifically, data has been collected related to readmisssion as well as other outcomes pertaining to patients with diabetes. What can we do to reduce these readmissions and possibly improve patient health?

<h3>Data Source</h3>

https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008 (Links to an external site.) - This data was donated in 2014 and is a collection of the past 6 years.
<h3>Modeling Techniques To Be Used:</h3>
Multi-class classification using one of Logistic Regression or Decision Trees, Counterfactual technique
<h3>Expected Results</h3>

I am expecting to find what are the important things (features) that contribute to a return/readmission. From this point, perhaps use the counterfactual explanations technique to determine what can possibly be changed to get a readmission score of False.
<h3>Why This Question Is Important</h3>

This question is important because individuals are being readmitted to hospitals for the same things. Particularly, in this case, these are diabetic patients. Diabetes is morbidity that needs to be watched closely and coupled with other issues that can lead to complexity and/or fatality. Thus, perhaps we can provide recommendations on changes to 1) keep the patient healthier and 2) keep readmissions down amongst diabetic patients.



Understanding the Data
From our data source, we are presented with various data from over 10 years of clinical care at 130 US hospitals and integrated delivery networks. It includes over 40 features representing patient and hospital outcomes. Information was extracted from the database for encounters that satisfied the following criteria:

It is an inpatient encounter (a hospital admission).
It is a diabetic encounter, that is, one during which any kind of diabetes was entered to the system as a diagnosis.
The length of stay was at least 1 day and at most 14 days.
Laboratory tests were performed during the encounter.
Medications were administered during the encounter.
The data contains such attributes as patient number, race, gender, age, admission type, time in hospital, medical specialty of admitting physician, number of lab test performed, HbA1c test result, diagnosis, number of medication, diabetic medications, number of outpatient, inpatient, and emergency visits in the year before the hospitalization, etc.

