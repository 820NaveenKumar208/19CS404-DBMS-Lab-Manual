# NAME : NAVEEN KUMAR T
# REG NO : 212223220067
# Experiment 1 : Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - Student Name

## Scenario Choose:
University / Hospital (choose one)

## ER Diagram:
ER Diagram for University

![alt text](439069612-6eb2a604-5304-4b26-a6da-69cc49be27a0.png)
## Entities and Attributes:
- Entity1: Attributes
- Entity2: Attributes
...

## Relationships and Constraints:
- Relationship1 (Cardinality, Participation)
- Relationship2 (Cardinality, Participation)
...

## Extension (Prerequisite / Billing):
- Explain how you modeled prerequisites or billing.

University Scenario
1. Modeling Prerequisites (Course Dependencies)
Entities & Relationships:
  Course (CourseID, Name, Credits)

   Prerequisite : A recursive relationship where one course is a prerequisite for another.
2. Modeling Billing (Fee Payments)
Entities & Relationships:
   Student (StudentID, Name, Email)
   Bill (BillID, Amount, DueDate, Status)
   Payment (PaymentID, Date, Amount, Method)

## Summary Table : 
![alt text](<Screenshot 2025-05-05 231639.png>)

## Design Choices:
Brief explanation of why you chose certain entities, relationships, and assumptions :
Entities :
1. Student
Represents individuals enrolled in the university.
Attributes: StudentID (PK), Name, Email, PhoneNumber, Program.
Essential for tracking course enrollments and billing information.

2. Course
Represents academic subjects offered.
Attributes: CourseID (PK), CourseName, Credits, DepartmentID (FK).
Central to modeling prerequisites and enrollments.

3. Professor
Represents faculty members teaching courses.
Attributes: ProfessorID (PK), Name, Email, DepartmentID (FK).
Links to courses they instruct.

4. Department
Represents academic divisions within the university.
Attributes: DepartmentID (PK), DepartmentName.
Organizes courses and professors.

5. Enrollment
Associative entity linking students and courses.
Attributes: EnrollmentID (PK), StudentID (FK), CourseID (FK), EnrollmentDate, Grade.
Captures enrollment details and grades.

6. Billing
Represents financial transactions for students.
Attributes: BillingID (PK), StudentID (FK), Amount, DueDate, Status.
Tracks tuition and other fees.

Relationships : 
1. Student–Enrollment–Course
Many-to-Many (M:N) relationship.
A student can enroll in multiple courses; a course can have multiple students.

2. Course–Prerequisite–Course
Recursive One-to-Many (1:N) relationship.
A course may require completion of another course.
Modeled using the Prerequisite entity.

3. Professor–Teaches–Course
One-to-Many (1:N) relationship.
A professor can teach multiple courses; each course is taught by one professor.
Links faculty to their courses.

4. Department–Offers–Course
One-to-Many (1:N) relationship.
A department offers multiple courses; each course belongs to one department.
Organizes courses under departments.

5. Student–Billing
One-to-Many (1:N) relationship.
A student can have multiple billing records.
Tracks financial obligations per student.

Assumptions :
1.Each student has a unique StudentID.
2.Courses have unique CourseIDs and belong to one department.
3.Professors are assigned to departments and teach multiple courses.
4.Enrollment records capture the many-to-many 
5.relationship between students and courses.
6.Billing records are generated per student for various fees.
E7.ach course is taught by one professor per term.
8.Departments oversee both courses and professors.
9.Grades are recorded within the Enrollment entity.
10.All entities and relationships are essential for comprehensive university data management.



## RESULT :
Therfore the ER diagram is created and implemented.
