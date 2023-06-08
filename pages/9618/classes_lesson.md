Certainly! Here's a step-by-step guide to help your students create the initial class for a person in a school, and then extend it to create classes for students, teaching staff, and non-teaching staff:

Step 1: Create the Person Class:
Start by creating a class called `Person` as the base class for all individuals in the school. Discuss with the students the common properties that every person in the school would have, such as `name`, `date_of_birth`, and `ID`. Here's an example code snippet to create the `Person` class:

```python
class Person:
    def __init__(self, name, date_of_birth, ID):
        self.name = name
        self.date_of_birth = date_of_birth
        self.ID = ID
```

Step 2: Discuss Specializations:
Engage the students in a discussion about the different roles within the school, such as students, teaching staff, and non-teaching staff. Talk about the unique properties that each role may have. For example, students may have a `grade` attribute, teaching staff may have a `subject_speciality` attribute, and non-teaching staff may have a `department` attribute.

Step 3: Create the Student Class:
Guide the students to create a `Student` class that inherits from the `Person` class. The `Student` class can add its own specific attributes, such as `grade` or `student_ID`. Here's an example code snippet:

```python
class Student(Person):
    def __init__(self, name, date_of_birth, ID, grade, student_ID):
        super().__init__(name, date_of_birth, ID)
        self.grade = grade
        self.student_ID = student_ID
```

Step 4: Create the TeachingStaff Class:
Similarly, help the students create a `TeachingStaff` class that inherits from `Person`. The `TeachingStaff` class can include additional attributes like `subject_speciality` or `employee_ID`. Here's an example code snippet:

```python
class TeachingStaff(Person):
    def __init__(self, name, date_of_birth, ID, subject_speciality, employee_ID):
        super().__init__(name, date_of_birth, ID)
        self.subject_speciality = subject_speciality
        self.employee_ID = employee_ID
```

Step 5: Create the NonTeachingStaff Class:
Lastly, guide the students to create a `NonTeachingStaff` class that inherits from `Person`. The `NonTeachingStaff` class can have specific attributes such as `department` or `employee_ID`. Here's an example code snippet:

```python
class NonTeachingStaff(Person):
    def __init__(self, name, date_of_birth, ID, department, employee_ID):
        super().__init__(name, date_of_birth, ID)
        self.department = department
        self.employee_ID = employee_ID
```

Step 6: Encourage Experimentation:
Encourage the students to experiment and add additional methods or attributes to each class as per their understanding and creativity. They can also create instances of the classes and test their implementations by printing out the values of the attributes.

This step-by-step guide will help your students create the initial `Person` class and then extend it to create specialized classes for students, teaching staff, and non-teaching staff, each with their own unique attributes. It allows them to understand how inheritance can help reuse and extend code, and how each class can have its own specific properties while sharing common attributes from the base class.