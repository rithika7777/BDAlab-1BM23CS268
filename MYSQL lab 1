create database hospital_db_CS259;
use hospital_db_CS259;

CREATE TABLE Patient (
    patient_id INT PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    gender CHAR(1),
    date_of_birth DATE,
    phone VARCHAR(15)
);
CREATE TABLE Lab_Report (
    report_id INT PRIMARY KEY,
    patient_id INT,
    test_name VARCHAR(100) NOT NULL,
    test_value VARCHAR(50),
    test_unit VARCHAR(20),
    test_date DATE,
    CONSTRAINT fk_lab_patient
        FOREIGN KEY (patient_id)
        REFERENCES Patient(patient_id)
        ON DELETE CASCADE
);
CREATE TABLE Medical_Image (
    image_id INT PRIMARY KEY,
    patient_id INT,
    image_type VARCHAR(50),
    body_part VARCHAR(50),
    image_date DATE,
    file_path VARCHAR(255),
    CONSTRAINT fk_image_patient
        FOREIGN KEY (patient_id)
        REFERENCES Patient(patient_id)
        ON DELETE CASCADE
);
