The aim of this training project is to analyse completed lessons. 
The analysis should answer these questions:

1. How many students have passed only one course successfully ? (Successfull pass is pass in an the examination)

2. What examinations were the hardest and the easiest? To find courses and examination within the course that the lowest and the highest completion rate*.

3. For each module to dtermine the average time for passing exams? (Passing is the last successfull completion of the exam)

4. To identify the most popular courses (TOP-3) by number of registrations and courses with the highest churn rate (TOP-3).

5. To write a function that allows to costract cohort (semester) analysis. Between early 2013 and late 2014 to identify the semester with the lowest course completition and the average course turnaround time. 
 
6. To construct RFM-clusters of students adapted to the learning objective , where R is the average exam turnaround time, F is course completation rate, M - the average score in an exam. To describe how clusters were created. 

*completion rate = number of successfull exams / number of all attemts to take the exam


Files: 

assessments.csv — the file contains information about the grades in the tests. Each course (module) usually includes a number of marks, followed by the final exam:

code_module — module id;
code_presentation — semester id;
id_assessment — test id;
assessment_type — test type. There are three type of assessment: teacher assessment (TMA), computer assessment (СМА), the final assessment of the course (Exam);
date — information about the test deadline. It's calculated as number of days since the start of the semester. The semester start date is numbered 0;
weight — assessment weight in %. Normally exams are considered separately and are weighted 100%; the sum of all other tests is 100%.

studentAssessment.csv — the file contains student's test results. If a student fails test or fails to send the result, the result isn't recordered in the table. Final exams are not accepted, if the result of the preliminary test isn't in the system:

id_student — student id;
date_submitted — the date of application by the student, measured as the number of days since the beginning of the semester;
is_banked — the fact that the student has retaken a test since the previous semester;
score — student's score in the test. The range is from 0 to 100. The score below 40 is interpreted as a failing grade.

studentRegistration.csv — the fail contains information about the time when a student registrated for this course within a semester:

code_module — module id;
code_presentation — semester id;
id_student — student id;
date_registration — student registration date is the number of days measured from start of the semester (for instance -30 means that a student registrated for the course 30 days before it started);
date_unregistration — the date of cancellation of the student's registration from the course. This field is blank for students who complited the module.
