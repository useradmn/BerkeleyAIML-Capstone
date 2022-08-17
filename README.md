# Capstone: Artificial Intelligence & Machine Learning
Professional Certificate
Haas School of Business
University of California, Berkeley
<hr>

<img align="center" src="https://www.signitysolutions.com/blog/wp-content/uploads/2020/09/artificial-intelligence-in-healthcare-sector.jpg">
<b>Overview:</b> In this capstone, my goal is to do the heavy lifting of the project. I will explore my data source, testa a few of the techniqueues, and com up with a solution or answer to my research problem. HTML version of notebook is <a href="https://federalcomputing.com/capstoneAIML.html" target="_blank">available here. </a>



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

<hr><br><br>
Our dataset is comprised of various features including demographics, relevant emergency room encounter information, medical drug data, etc. Our features are listed below.<br><br>

<h3>Features:</h3>

+ <b>race</b></b> - The race of the patient
+ <b>gender</b> - The gender of the patient (some marked as unknown)
+ <b>age</b> - The age of the patient
+ <b>admission_type_id</b> - Integer identifier corresponding to 9 distinct values, for example, emergency, urgent, elective, newborn, and not available
+ <b>discharge_disposition_id</b> - Integer identifier corresponding to 29 distinct values, for example, discharged to home, expired, and not available
+ <b>admission_source_id</b> - Integer identifier corresponding to 21 distinct values, for example, physician referral, emergency room, and transfer from a hospital
+ <b>time_in_hospital</b> - Integer number of days between admission and discharge
+ <b>medical_specialty</b> - Integer identifier of a specialty of the admitting physician, corresponding to 84 distinct values, for example, cardiology, internal medicine, family/general practice, and surgeon
+ <b>num_lab_procedures</b> - Number of lab tests performed during the encounter
+ <b>num_procedures</b> - Number of procedures (other than lab tests) performed during the encounter
+ <b>num_medications</b> - Number of distinct generic names administered during the encounter
+ <b>number_outpatient</b> - Number of outpatient visits of the patient in the year preceding the encounter
+ <b>number_emergency</b> - Number of emergency visits of the patient in the year preceding the encounter
+ <b>number_inpatient</b> - Number of inpatient visits of the patient in the year preceding the encounter
+ <b>diag_1</b> - The primary diagnosis (coded as first three digits of ICD9); 848 distinct values
+ <b>diag_2</b> - Secondary diagnosis (coded as first three digits of ICD9); 923 distinct values
+ <b>diag_3</b> - Additional secondary diagnosis (coded as first three digits of ICD9); 954 distinct values
+ <b>number_diagnoses</b> - Number of diagnoses entered to the system 0%
+ <b>max_glu_serum</b> - Indicates the range of the result or if the test was not taken. Values: “>200,” “>300,” “normal,” and “none” if not measured
+ <b>A1Cresult</b> - Indicates the range of the result or if the test was not taken. Values: “>8” if the result was greater than 8%, “>7” if the result was greater than 7% but less than 8%, “normal” if the result was less than 7%, and “none” if not measured.
+ <b>metformin</b> - medical drug
+ <b>repaglinide</b> - medical drug
+ <b>nateglinide</b> - medical drug
+ <b>chlorpropamide</b> - medical drug
+ <b>glimepiride</b> - medical drug
+ <b>acetohexamide</b> - medical drug
+ <b>glipizide</b> - medical drug
+ <b>glyburide</b> - medical drug
+ <b>tolbutamide</b> - medical drug
+ <b>pioglitazone</b> - medical drug
+ <b>rosiglitazone</b> - medical drug
+ <b>acarbose</b> - medical drug
+ <b>miglitol</b> - medical drug
+ <b>troglitazone</b> - medical drug
+ <b>tolazamide</b> - medical drug
+ <b>examide</b> - medical drug
+ <b>citoglipton</b> - medical drug
+ <b>insulin</b> - medical drug
+ <b>glyburide-metformin</b> - medical drug
+ <b>glipizide-metformin</b> - medical drug
+ <b>glimepiride-pioglitazone</b> - medical drug
+ <b>metformin-rosiglitazone</b> - medical drug
+ <b>metformin-pioglitazone</b> - medical drug
+ <b>change</b> - Indicates if there was a change in diabetic medications (either dosage or generic name). Values: “change” and “no change”
+ <b>diabetesMed</b> - Indicates if there was any diabetic medication prescribed. Values: “yes” and “no”
<br><br>
 <h3>Understanding the Data</h3>
From our data source, we are presented with various data from over 10 years of clinical care at 130 US hospitals and integrated delivery networks. It includes over 40 features representing patient and hospital outcomes. Information was extracted from the database for encounters that satisfied the following criteria:

+ It is an inpatient encounter (a hospital admission).
+ It is a diabetic encounter, that is, one during which any kind of diabetes was entered to the system as a diagnosis.
+ The length of stay was at least 1 day and at most 14 days.
+ Laboratory tests were performed during the encounter.
+ Medications were administered during the encounter.
+ The data contains such attributes as patient number, race, gender, age, admission type, time in hospital, medical specialty of admitting physician, number of lab test performed, HbA1c test result, diagnosis, number of medication, diabetic medications, number of outpatient, inpatient, and emergency visits in the year before the hospitalization, etc.
<hr><br><br>
<h2>Modeling<h3><br>
<b>A baseline analysis:</b><br>
Training time :[0.0029990673065185547]
Training accuracy :[0.4976837554045707]
Test accuracy :[0.49924664264657714]
Accuracy score : Not Yet Available
AUC score : Not Yet Available<br><br>
#################LOGISTIC REGRESSION ANALYSIS##########

Training time :3.8975634574890137
Training accuracy :0.6180582851367287
Test accuracy :0.6188994431706518
Accuracy score : 0.6188994431706518
AUC score : 0.6034773037012175

######################################################<br><br>
 <img src="https://awesomescreenshot.s3.amazonaws.com/image/3446742/31431676-490548cfd16b6a5484cd60a39f153edb.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220816%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220816T185414Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=5c161a76e8fa5289725b93f343fa452796a4843e650621345637564c52d32786">
 <br>
 <h3>Feature Importance</h3>
Feature: race 	 Score:-0.033796467119041725
<br>Feature: gender 	 Score:0.05220811772492702
<br>Feature: age 	 Score:0.0029344954582298266
<br>Feature: admission_type_id 	 Score:0.032138882815709854
<br>Feature: discharge_disposition_id 	 Score:-0.012756074107160375
<br>Feature: admission_source_id 	 Score:0.005697368221586632
<br>Feature: time_in_hospital 	 Score:0.015309280096100903
<br>Feature: medical_specialty 	 Score:0.0009692045401855414
<br>Feature: num_lab_procedures 	 Score:0.0009561158077616839
<br>Feature: num_procedures 	 Score:-0.04584900082060058
<br>Feature: num_medications 	 Score:0.0009861661339249123
<br>Feature: number_outpatient 	 Score:0.08235667848348943
<br>Feature: number_emergency 	 Score:0.1888097939190253
<br>Feature: number_inpatient 	 Score:0.3728662559579259
<br>Feature: diag_1 	 Score:-0.00013084404297845518
<br>Feature: diag_2 	 Score:-0.00016948616423528032
<br>Feature: diag_3 	 Score:3.229928653600553e-05
<br>Feature: number_diagnoses 	 Score:0.08312833535252362
<br>Feature: max_glu_serum 	 Score:-0.0191027671164415
<br>Feature: A1Cresult 	 Score:-0.02281927899061262
<br>Feature: metformin 	 Score:-0.11773066366763427
<br>Feature: repaglinide 	 Score:-0.016584307605706474
<br>Feature: nateglinide 	 Score:-0.19847540350258402
<br>Feature: chlorpropamide 	 Score:-0.2624410900601061
<br>Feature: glimepiride 	 Score:-0.02035639009589943
<br>Feature: acetohexamide 	 Score:0.004290645238704124
<br>Feature: glipizide 	 Score:0.06904377139404178
<br>Feature: glyburide 	 Score:0.007883757005958742
<br>Feature: tolbutamide 	 Score:-0.023482659033740666
<br>Feature: pioglitazone 	 Score:0.0760129295032895
<br>Feature: rosiglitazone 	 Score:0.06253838495541769
<br>Feature: acarbose 	 Score:-0.16133545826556323
<br>Feature: miglitol 	 Score:-0.3045983331251128
<br>Feature: troglitazone 	 Score:0.004864037064982501
<br>Feature: tolazamide 	 Score:-0.00474502797746427
<br>Feature: examide 	 Score:0.0
<br>Feature: citoglipton 	 Score:0.0
<br>Feature: insulin 	 Score:-0.0677520106092102
<br>Feature: glyburide-metformin 	 Score:-0.14107438654274135
<br>Feature: glipizide-metformin 	 Score:0.004826525999850238
<br>Feature: glimepiride-pioglitazone 	 Score:0.003183159044823325
<br>Feature: metformin-rosiglitazone 	 Score:-0.0030582987827478575
<br>Feature: metformin-pioglitazone 	 Score:-0.0028793596105040455
<br>Feature: change 	 Score:-0.046693629295805776
<br>Feature: diabetesMed 	 Score:0.2760422737557418
<br><b>Feature importance:</b><br>
<img src="https://awesomescreenshot.s3.amazonaws.com/image/3446742/31431825-7ee92e560ab411fbdd023b42739ba9bb.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220816%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220816T185851Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=a174c2b457274f40ffabe6cab4f16250d08c83d6d4ec43054d0a02683772f195"><br><br>
<hr><br><br>
<h3>Decision Tree Coefficients</h3>
<img src="https://awesomescreenshot.s3.amazonaws.com/image/3446742/31464314-e6073327166ea16281fbfc3c89e65253.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220817%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220817T142446Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=cfa1dfefa0a26b01fb1ed539e52e3c2b7ab5d4ee917415d0ab2bf17609cef2e3"><br>
