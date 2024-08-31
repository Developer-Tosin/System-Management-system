
# Student Management System

## Overview

The Student Management System is a simple application built using Object-Oriented Programming (OOP) principles in Python. This system allows for the management of students, instructors, courses, and enrollments. The project demonstrates the use of classes, objects, inheritance, polymorphism, and encapsulation.

## Features

- **Manage Students:** Add, remove, and update student information.
- **Manage Instructors:** Add, remove, and update instructor information.
- **Manage Courses:** Add, remove, and update courses.
- **Enroll Students:** Enroll students in courses.
- **Assign Grades:** Assign grades to students for specific courses.
- **Retrieve Information:**
  - List of students enrolled in a specific course.
  - List of courses a specific student is enrolled in.

## Class Structure

### 1. `Person`
- **Attributes:**
  - `name` (str): The name of the person.
  - `id_number` (str): The unique ID number of the person.
- **Methods:**
  - `__str__`: Returns a string representation of the person.

### 2. `Student` (inherits from `Person`)
- **Attributes:**
  - `major` (str): The major of the student.
- **Methods:**
  - `__str__`: Returns a string representation of the student, including their major.

### 3. `Instructor` (inherits from `Person`)
- **Attributes:**
  - `department` (str): The department of the instructor.
- **Methods:**
  - `__str__`: Returns a string representation of the instructor, including their department.

### 4. `Course`
- **Attributes:**
  - `course_name` (str): The name of the course.
  - `course_id` (str): The unique ID of the course.
  - `enrolled_students` (list): A list of students enrolled in the course.
- **Methods:**
  - `add_student(student)`: Adds a student to the course.
  - `remove_student(student)`: Removes a student from the course.
  - `__str__`: Returns a string representation of the course, including enrolled students.

### 5. `Enrollment`
- **Attributes:**
  - `student` (Student): The student enrolled in the course.
  - `course` (Course): The course in which the student is enrolled.
  - `grade` (str, optional): The grade assigned to the student (initially set to `None`).
- **Methods:**
  - `assign_grade(grade)`: Assigns a grade to the student.
  - `__str__`: Returns a string representation of the enrollment.

### 6. `StudentManagementSystem`
- **Attributes:**
  - `students` (list): A list of all students.
  - `instructors` (list): A list of all instructors.
  - `courses` (list): A list of all courses.
  - `enrollments` (list): A list of all enrollments.
- **Methods:**
  - `add_student(student)`: Adds a student to the system.
  - `remove_student(student)`: Removes a student from the system.
  - `update_student(student, name=None, major=None)`: Updates a student's information.
  - `add_instructor(instructor)`: Adds an instructor to the system.
  - `remove_instructor(instructor)`: Removes an instructor from the system.
  - `update_instructor(instructor, name=None, department=None)`: Updates an instructor's information.
  - `add_course(course)`: Adds a course to the system.
  - `remove_course(course)`: Removes a course from the system.
  - `update_course(course, course_name=None, course_id=None)`: Updates a course's information.
  - `enroll_student(student, course)`: Enrolls a student in a course.
  - `assign_grade(student, course, grade)`: Assigns a grade to a student in a course.
  - `get_students_in_course(course)`: Retrieves a list of students enrolled in a specific course.
  - `get_courses_for_student(student)`: Retrieves a list of courses a specific student is enrolled in.

