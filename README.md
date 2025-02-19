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
(Insert DFD here)

### b. Context-Level Entity Relationship Diagram
(Insert ERD here)

### c. Use Cases

#### i. Use Case Scenarios

1. **Apply to University**
   - **Actors:** Applicant, Admissions Office
   - **Description:** As a prospective student, I want to submit an application online so that I can be considered for admission.

2. **Schedule Classes**
   - **Actors:** Student, Registrar System
   - **Description:** As a student, I want to schedule classes so that I can complete my degree requirements.

3. **Withdraw from a Class**
   - **Actors:** Student, Academic Advisor
   - **Description:** As a student, I want to withdraw from a class so that I can adjust my academic plan.

4. **Submit Final Grades**
   - **Actors:** Faculty, Registrar
   - **Description:** As a faculty member, I want to submit final grades so that student records are updated.

5. **Change Major**
   - **Actors:** Student, Academic Advisor
   - **Description:** As a student, I want to submit a major change request so that I can switch academic programs.

6. **View Transcript**
   - **Actors:** Student, Registrar
   - **Description:** As a student, I want to view my transcript so that I can track my academic progress.

7. **Apply for Graduation**
   - **Actors:** Student, Registrar
   - **Description:** As a student, I want to apply for graduation so that I can receive my degree.

8. **Check Graduation Requirements**
   - **Actors:** Student, Registrar
   - **Description:** As a student, I want to check my graduation requirements so that I know what courses I still need to complete.

9. **Submit FAFSA**
   - **Actors:** Student, Financial Aid Office
   - **Description:** As a student, I want to submit my FAFSA so that I can receive financial aid.

#### ii. Use Case Diagram
(Insert Use Case Diagram here)

---

## 4. Conclusion
This document lays out the initial system proposal, covering its key functions, interactions, and data relationships. Future phases will refine these details and develop a more comprehensive system design.

