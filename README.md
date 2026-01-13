STUDENT(
  rollno INT PRIMARY KEY,
  name VARCHAR(50),
  dept VARCHAR(10),
  year INT
);

COURSE(
  course_id INT PRIMARY KEY,
  course_name VARCHAR(50),
  credits INT
);

ENROLLMENT(
  rollno INT,
  course_id INT,
  marks INT,
  PRIMARY KEY (rollno, course_id),
  FOREIGN KEY (rollno) REFERENCES STUDENT(rollno),
  FOREIGN KEY (course_id) REFERENCES COURSE(course_id)
);

Write an SQL query to display the names of students who have scored more than the average marks of their respective courses.
