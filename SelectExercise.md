1. Selezionare tutti gli studenti nati nel 1990 (160)

SELECT `date_of_birth` FROM `149_db_university`.`students`
WHERE date_of_birth BETWEEN '1990-1-1' AND '1990-12-31'


2. Selezionare tutti i corsi che valgono più di 10 crediti (479)
   
    SELECT 
    `courses`.`name`,
    `courses`.`cfu`
FROM `149_db_university`.`courses`
WHERE CFU > 10

3. Selezionare tutti gli studenti che hanno più di 30 anni

     SELECT `date_of_birth` FROM `149_db_university`.`students`
WHERE date_of_birth > '1995-12-5'

4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
laurea (286)

    SELECT courses.name
FROM `149_db_university`.`courses`
WHERE period = 'I semestre' AND year = '1'

1. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020 (21)

    SELECT `exams`.`id`, `exams`.`hour`, `exams`.`date` 
 FROM 149_db_university.exams
 WHERE hour > TIME("14:00:00") AND date = DATE("2020/06/20")

1. Selezionare tutti i corsi di laurea magistrale (38)
2. Da quanti dipartimenti è composta l'università? (12)
3. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)