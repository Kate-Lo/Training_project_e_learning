The purpouse of this training project is to analyze completed lessons and answer the following questions:

1. Which test was the most difficult? And which test was the easiest?
2. Which module was the most difficult? And which module was the easiest?
3. Which modules are the most popular (TOP-3)? And which modules have the highest churn rate (TOP-3)?
4. Does students usually pass tests on time?
5. Create RFM-clusters of students adapted to the learning objective. 


Files: 

assessments.csv — the file contains information about the grades in the tests:

code_module — module id;
code_presentation — semester id;
id_assessment — test id;
assessment_type — test type. There are three types of assessments: teacher assessment (TMA), computer assessment (СМА), the final assessment of the module (Exam);
date — the test deadline. It's calculated as number of days since the start of the semester. The semester start date is numbered 0;
weight — assessment weight in %. Normally exams are considered separately and are weighted 100%; the sum of all other tests is 100%.


studentAssessment.csv — the file contains student's test results. If a student fails test or fails to send the result, the result isn't recordered in the table. Final exams are not accepted, if the result of the midterm test isn't in the system:

id_student — student id;
date_submitted — the date the student passed the test, measured as the number of days since the beginning of the semester;
is_banked — the fact of re-crediting the test from the previous semester;
score — student's score in the test. The range is from 0 to 100. The score below 40 is interpreted as a failing grade.

studentRegistration.csv — the file contains information about the time of registration for the module:

code_module — module id;
code_presentation — semester id;
id_student — student id;
date_registration — student registration date is the number of days measured from start of the semester (for instance -30 means that a student registrated for the course 30 days before it started);
date_unregistration — the date of cancellation of the student's registration from the module. This field is blank for students who complited the module.
