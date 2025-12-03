Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università:
- sono presenti diversi `Dipartimenti` (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
- ogni `Dipartimento` offre più `Corsi di Laurea` (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
- ogni `Corso di Laurea` prevede diversi `Corsi` (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
- ogni `Corso` può essere tenuto da diversi `Insegnanti`;
- ogni `Corso` prevede più appelli d'`Esame`;
- ogni `Studente` è iscritto ad un solo `Corso di Laurea`;
- ogni `Studente` può iscriversi a più appelli di `Esame`;
- per ogni appello d'`Esame` a cui lo `Studente` ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente.
Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.


## Tables

- Departments
- Degree
- Courses
- Teachers
- Exams
- Students

## Departments
 
- id INT PK UNIQUE
- name VARCHAR(100) NOTNULL
- Address VARCHAR(255)
- Degree VARCHAR(255)

## Degree

- id INT PK UNIQUE
- Course VARCHAR(255)
- Remote_or_onsite TINYINT (Considerandolo un booleano)
- Years_of_durations TINYINT
- which_building VARCHAR(255)

## Courses

- id INT PK UNIQUE
- number_of_students TINYINT
- is_open <!--Meaning if an entry test is needed--> TINYINT (Considerandolo un booleano)
- teacher_id INT PK

## Teacher

- id INT PK UNIQUE
- Name VARCHAR(255)
- Lastname VARCHAR(255)
- Subject VARCHAR(150)

## Student

- id BIGINT PK UNIQUE
- Name VARCHAR(255)
- Lastname VARCHAR(255)
- Degree VARCHAR(255)
- Immatricolation_year YEAR

## Exam

- id INT PK UNIQUE
- Student_id INT FK
- result TINYINT