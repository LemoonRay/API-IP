TABLE CREATION

CREATE TABLE students ( 
    id INT AUTO_INCREMENT PRIMARY KEY, 
    name VARCHAR(100) NOT NULL, 
    midterm_score FLOAT NOT NULL, 
    final_score FLOAT NOT NULL, 
    final_grade FLOAT AS ((0.4 * midterm_score) + (0.6 * final_score)) STORED, 
    status VARCHAR(10) AS (CASE WHEN final_grade >= 75 THEN 'Pass' ELSE 'Fail' END) STORED 
);


