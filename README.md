#!/bin/bash
# Download the MySQL repository package
wget https://dev.mysql.com/get/mysql80-community-release-el9-5.noarch.rpm
# Install the MySQL repository package
sudo dnf install mysql80-community-release-el9-5.noarch.rpm -y
# Enable the MySQL community repository
sudo dnf repolist enabled | grep "mysql.*-community.*"
# Install MySQL
sudo dnf install mysql -y	


mysql -h myauroracluster.cluster-cu8ff7u11ko4.us-east-1.rds.amazonaws.com -u WhizlabsAdmin -pWhizlabs123


Create database auroro_db;
use auroro_db;
Show databases;

CREATE TABLE students ( subject_id INT AUTO_INCREMENT, subject_name VARCHAR(255) NOT NULL,  teacher VARCHAR(255),start_date DATE, lesson TEXT,PRIMARY KEY (subject_id));
		
Select * from students;

INSERT INTO students(subject_name, teacher) VALUES ('English', 'Vinay');
INSERT INTO students(subject_name, teacher) VALUES ('Science', 'Vidhi');
INSERT INTO students(subject_name, teacher) VALUES ('Maths', 'Div');
INSERT INTO students(subject_name, teacher) VALUES ('Arts', 'Spruha');


select * from students;
