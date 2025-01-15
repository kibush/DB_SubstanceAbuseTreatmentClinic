# Substance AbuseTreatment Clinic DB design
 Project to design a database for small substance abuse clinic.
Substance Abuse Treatment Center
For our proposed  project  the  clinical IT system used was ideally for  a substance abuse treatment program which included  workflow related to patient intake, assessment, treatment planning, and progress tracking. The  tasks that were  included in these workflows were  as follows :
•Patient intake: This involved collecting basic demographic and contact information from patients, as well as information about their substance abuse history and current symptoms.
•Assessment: This also  involved  evaluating patients to determine their level of substance abuse, the severity of their addiction, and any co-occurring mental health disorders.
•Treatment planning: Based on the assessment, a treatment plan was  developed that outlined the specific goals of treatment and the interventions that would  be used to achieve them.
•Progress tracking: This involved  collecting data on patients' progress during treatment and using it to adjust the treatment plan as needed.


Key Components of the Database Design
Entities and Tables:
The following entities represent the key components of the workflows:

Patients: Stores demographic and contact information, substance abuse history, and current symptoms.
Assessments: Records evaluations of patients, including the level of substance abuse, severity of addiction, and co-occurring disorders.
Treatment Plans: Contains individualized treatment goals, selected interventions, and treatment start and end dates.
Progress Notes: Tracks patient progress, including session outcomes, attendance, and updates to the treatment plan.
Staff: Stores information about clinic staff members responsible for assessments, treatment, and progress tracking.
Attributes for Each Table:

Patients Table: Patient ID, name, date of birth, gender, contact details, substance abuse history, current symptoms, intake date.
Assessments Table: Assessment ID, patient ID (foreign key), date of assessment, addiction severity, co-occurring disorders, notes.
Treatment Plans Table: Plan ID, patient ID (foreign key), treatment goals, interventions, assigned clinician ID (foreign key to Staff table), start date, end date.
Progress Notes Table: Progress ID, patient ID (foreign key), session date, clinician ID (foreign key), session notes, changes to the treatment plan.
Staff Table: Staff ID, name, role, contact information, credentials.
Relationships:

One-to-Many Relationships:
A patient can have multiple assessments, treatment plans, and progress notes.
Staff can work with multiple patients for assessments, treatment planning, and progress tracking.
Foreign Keys:
Patient ID links Patients table to Assessments, Treatment Plans, and Progress Notes.
Staff ID links the Staff table to other tables to indicate who performed specific tasks.
Workflow and Functionality Integration
Patient Intake:

A form collects patient demographic details, contact information, and substance abuse history. This data is stored in the Patients table.
Assessment:

Clinicians conduct an evaluation and document addiction severity and co-occurring disorders. Results are stored in the Assessments table.
Treatment Planning:

Based on the assessment, clinicians develop a plan and record goals and interventions in the Treatment Plans table. Staff IDs are associated to track accountability.
Progress Tracking:

Clinicians log session notes, track attendance, and document progress in the Progress Notes table. Any changes to treatment plans are also updated.
  

