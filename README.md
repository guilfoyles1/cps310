# CPS 310 - Phase 1: System Overview & Use Cases

## Authors
- Claire Summers
- Mason Euler
- Shayna Guilfoyle

## 1. Introduction

### a. Purpose
This document lays out a proposed system improvement for the University of Dayton’s student services. As students, we’ve all dealt with the headaches of applying, scheduling, withdrawing, and tracking grades. This system aims to simplify those processes and make life a little easier for everyone involved.

### b. Scope
This document covers an initial analysis of the system, including a context-level data flow diagram, an entity relationship model, and detailed use cases. It won’t go into implementation specifics but sets the foundation for system design.

### c. Definitions & Acronyms
- **DFD (Data Flow Diagram)**: A diagram showing how data moves through the system.
- **ERD (Entity Relationship Diagram)**: A visualization of the relationships between different system components.
- **Use Case**: A scenario that describes interactions between users and the system.
- **UD (University of Dayton)**: The institution this system is designed for.

### d. References
- University of Dayton student services documentation
- Class lectures and notes
- Canvas discussion board for user feedback

### e. Overview
This document is broken into sections that outline the system’s environment, functionality, and user interactions. It also includes diagrams that visually represent the system structure and use cases.

---

## 2. Overall Description

### a. Product Perspective
This system will integrate with existing UD services like the application portal, course scheduling system, and graduation management tools. The goal is to create a seamless, user-friendly experience.

### b. Product Functions
The system will handle:
- Submitting and tracking university applications
- Scheduling and managing courses
- Withdrawing from courses
- Submitting and accessing final grades
- Managing major change requests
- Viewing transcripts
- Applying for graduation
- Checking graduation requirements
- Submitting FAFSA

### c. User Characteristics
- **Students:** The primary users who interact with the system for scheduling, grades, and graduation.
- **Faculty & Advisors:** Responsible for approving class changes, major changes, and submitting grades.
- **Administrators:** Oversee applications, course availability, and graduation approvals.

### d. Constraints
- Must work with UD’s existing databases and authentication system.
- Needs to be accessible on both desktop and mobile.
- Must comply with FERPA regulations.

### e. Assumptions
- Users will have a basic understanding of online student systems.
- Existing student records and authentication will be used.
- The system will primarily serve current and prospective students, faculty, and staff.

---

## 3. Systems Analysis

### a. Context-Level Data Flow Diagram
![DFD_CPS310](https://github.com/user-attachments/assets/713c75c5-f604-44f4-9060-2f6f7ddcb620)

### b. Context-Level Entity Relationship Diagram
![ER Diagram](https://github.com/guilfoyles1/cps310/blob/main/ERD.png)


### c. Use Cases

#### i. Use Case Scenarios

1. **Apply to University**
   - **Actors:** Student, Administration  
   - **Description:** As a prospective student, I want to submit an application online so that I can be considered for admission.  
   - **Trigger:** The student decides to apply to a university.  
   - **Preconditions:**  
      - The university’s application portal must be operational.  
      - The student must have access to required documents (transcripts, essays, etc.).  
   - **Steps:**  
      1. The student accesses the university’s admissions portal.  
      2. The student creates an account or logs into an existing account.  
      3. The student fills out the application form.  
      4. The student uploads required documents.  
      5. The student pays the application fee (if applicable).  
      6. The student submits the application.  
      7. The administration reviews the application and provides an acknowledgment.  
   - **Postconditions:**  
      - The application is stored in the admissions system.  
      - The student receives a confirmation email or notification.  
   - **Assumptions:**  
      - The payment system for application fees is functioning properly.  

---

2. **Schedule Classes**
   - **Actors:** Student, Administration  
   - **Description:** As a student, I want to schedule classes so that I can complete my degree requirements.  
   - **Trigger:** The course registration period begins, or the student needs to modify their schedule.  
   - **Preconditions:**  
      - The student must be an active, enrolled student.  
      - The registration system must be available.  
   - **Steps:**  
      1. The student logs into the registration system.  
      2. The student searches for available courses.  
      3. The student selects desired courses.  
      4. The system checks for prerequisites and time conflicts.  
      5. The student confirms their schedule and submits the registration.  
      6. The system updates the student’s schedule and generates a confirmation.  
   - **Postconditions:**  
      - The student’s course schedule is updated in the system.  
      - The student receives a confirmation of their registered classes.  
   - **Assumptions:**  
      - Course seats are available.  

---

3. **Withdraw from a Class**
   - **Actors:** Student, Administration  
   - **Description:** As a student, I want to withdraw from a class so that I can adjust my academic plan.  
   - **Trigger:** The student decides they no longer want to continue a class.  
   - **Preconditions:**  
      - The withdrawal period must be open.  
   - **Steps:**  
      1. The student logs into the academic portal.  
      2. The student navigates to their class schedule.  
      3. The student selects the class they want to withdraw from.  
      4. If required, the system notifies administration for approval.  
      5. The administration reviews the request and provides guidance.  
      6. Upon approval, the system processes the withdrawal and updates the student’s record.  
   - **Postconditions:**  
      - The class is removed from the student’s active schedule.  
      - The student’s transcript reflects a withdrawal (if applicable).  
   - **Assumptions:**  
      - The student understands the financial and academic consequences of withdrawing.  

---

4. **Submit Final Grades**
   - **Actors:** Faculty, Administration  
   - **Description:** As a professor, I want to submit final grades so that student records are updated.  
   - **Trigger:** The end of the academic term is reached.  
   - **Preconditions:**  
      - The professor must have access to the grading system.  
   - **Steps:**  
      1. The professor logs into the grading system.  
      2. The professor selects the course they are teaching.  
      3. The professor enters final grades for each student.  
      4. The professor reviews and confirms the submitted grades.  
      5. The system updates student records and notifies administration.  
   - **Postconditions:**  
      - The students’ transcripts are updated with final grades.  
      - Administration has access to the submitted grades for official records.  

---

5. **Change Major**
   - **Actors:** Student, Administration  
   - **Description:** As a student, I want to submit a major change request so that I can switch academic programs.  
   - **Trigger:** The student decides to change their major.  
   - **Steps:**  
      1. The student schedules a meeting with an advisor.  
      2. The advisor reviews the student’s request and provides guidance.  
      3. The student submits a major change request form.  
      4. Administration approves the request.  
      5. The system updates the student’s academic record.  
      6. The student receives confirmation of the major change.  

---

6. **View Transcript**
   - **Actors:** Student, Administration  
   - **Description:** As a student, I want to view my transcript so that I can track my academic progress.  
   - **Trigger:** The student wants to check their academic history.  
   - **Steps:**  
      1. The student logs into the student portal.  
      2. The student navigates to the transcript section.  
      3. The system retrieves and displays the student's academic record.  
      4. The student can view, download, or request an official transcript.  

---

7. **Apply for Graduation**
   - **Actors:** Student, Administration  
   - **Description:** As a student, I want to apply for graduation so that I can receive my degree.  
   - **Trigger:** The student reaches the final semester of their program.  
   - **Preconditions:**  
      - The student must have completed (or be on track to complete) all graduation requirements.  
   - **Steps:**  
      1. The student logs into the academic portal.  
      2. The student verifies that they have met all graduation requirements.  
      3. The student fills out and submits the graduation application.  
      4. Administration reviews the application.  
      5. The student receives confirmation of application approval or notification of missing requirements.  
      6. If approved, the student receives further instructions on commencement and diploma issuance.  
   - **Postconditions:**  
      - The student’s graduation status is recorded.  

---

8. **Check Graduation Requirements**
   - **Actors:** Student, Administration  
   - **Description:** As a student, I want to check my graduation requirements so that I know what courses I still need to complete.  
   - **Trigger:** The student wants to verify their progress toward graduation.  
   - **Steps:**  
      1. The student logs into the academic portal.  
      2. The student navigates to the degree audit section.  
      3. The system displays completed and remaining graduation requirements.  
      4. The student reviews the information and consults an advisor if needed.  

---

9. **Submit FAFSA**
   - **Actors:** Student, Administration  
   - **Description:** As a student, I want to submit my FAFSA so that I can receive financial aid.  
   - **Trigger:** The FAFSA application period begins or the student needs financial aid.  
   - **Preconditions:**  
      - The student must have a valid Social Security Number (or eligible non-citizen status).  
   - **Steps:**  
      1. The student accesses the FAFSA website.  
      2. The student logs in or creates an account.  
      3. The student fills out the FAFSA form, including financial and personal information.  
      4. The student submits required documentation (e.g., tax returns, income verification).  
      5. The system processes the application and generates a confirmation.  
      6. Administration receives and reviews the application.  
      7. The student is notified of their financial aid award status.  
   - **Postconditions:**  
      - The FAFSA application is submitted and processed.  

#### ii. Use Case Diagram
![Use Case Diagram](https://github.com/guilfoyles1/cps310/blob/main/UseCaseDiagram.png)

---

## 4. Conclusion
This document lays out the initial system proposal, covering its key functions, interactions, and data relationships. Future phases will refine these details and develop a more comprehensive system design.

