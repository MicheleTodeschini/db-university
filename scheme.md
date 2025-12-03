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

- id
- name
- Address
- Degree

## Degree

- id
- Course
- Remote_or_onsite
- Years_of_durations
- which_building

## Courses

- id
- number_of_students
- is_open <!--Meaning if an entry test is needed-->
- teacher_id

## Teacher

- id
- Name
- Lastname
- Subject

## Student

- id
- Name
- Lastname
- Department
- Degree
- Course
- Immatricolation_year

## Exam

- id
- Student_id
- result