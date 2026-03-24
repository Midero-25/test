# Datubāzu modelēšana un normalizācija

![SQL](https://img.shields.io/badge/Language-SQL-blue) ![PHP](https://img.shields.io/badge/Language-PHP-777bb4) ![Excel](https://img.shields.io/badge/Tools-MS_Excel-green)

Šis repozitorijs satur mācību materiālus par datubāzu projektēšanu, ER diagrammām un datu normalizāciju (1NF - 3NF).

---

## Materiālu struktūra

### 1. Teorija
* **[Datubāzu modelēšana un normalizācija (1).pdf](./Datubāzu%20modelēšana%20un%20normalizācija%20(1).pdf)**
    * ER diagrammu pamati.
    * Normalizācijas soļi un noteikumi.
    * Uzdevumu nosacījumi un atbildes uz tiem.

### 2. Praktiskais kods
* **[db students.docx](./db%20students.docx)**
    * SQL skripti tabulu izveidei (`CREATE TABLE`) un datu aizpildei.
    * PHP piemērs datu atlasei no datubāzes.
    * HTML lapas skripts, kur var parbaudīt izveidotas datubāzes struktūru. 

### 3. Praktiskie uzdevumi
* **[Uzdevumi_normalizācija.xlsx](./Uzdevumi_normalizācija.xlsx)**
    * 7 interaktīvi uzdevumi Excel vidē datu transformēšanai.

---

## Uzstādīšana un lietošana

Lai palaistu praktisko daļu (SQL/PHP):
1.  Lejupielādējiet un palaidiet **WAMP** serveri.
2.  Importējiet SQL kodu no Word faila savā `phpMyAdmin` vidē.
3.  Pārliecinieties, ka PHP skripts ir ievietots jūsu servera mapē.
4.  Servera mapē "C:\wamp64\www\student_checker" Izveidot HTML lapu, kuras skripts ir word dokumentā.

---

## Refleksija
Nodarbības beigās studenti tiek aicināti aizpildīt refleksijas karti:

![Refleksija](./REFLEKSIJA.png)


# Lietotāja ceļvedis: Datubāzu modelēšana un normalizācija

Šis materiālu komplekts ir paredzēts, lai apgūtu datubāzu projektēšanas pamatus, ER diagrammu izveidi un datu normalizāciju (1NF, 2NF, 3NF), kā arī praktisko darbu ar SQL un PHP WampServer vidē.

---

## 1. Materiālu pārskats

| Fails | Saturs un mērķis |
| :--- | :--- |
| **Teorija (PDF)** | Prezentācija ar galvenajiem jēdzieniem, ER diagrammu piemēriem un normalizācijas soļiem. |
| **Uzdevumi (Excel)** | Interaktīva vide, kurā skolēni praktiski veic datu sadalīšanu tabulās (1.–7. uzdevums). |
| **db students (Word)** | SQL vaicājumi tabulu izveidei un PHP kods datu attēlošanai mājaslapā. |
| **Refleksija (Attēls)** | Materiāls stundas noslēgumam, lai izvērtētu apgūto. |

---

## 2. Darba uzsākšana ar WampServer

Lai praktiski izpildītu uzdevumus, ir nepieciešams strādāt ar **WampServer** (vai līdzīgu lokālo serveri).

### 2.1. Datubāzes izveide (phpMyAdmin)
1.  **Palaid WampServer**: Pārliecinies, ka ikona sistēmas joslā ir **zaļā krāsā**.
2.  Atver **phpMyAdmin** (parasti pārlūkprogrammā ierakstot `localhost/phpmyadmin`).
3.  Pieslēdzies (noklusējuma lietotājvārds: `root`, parole: tukša).
4.  Sānjoslā spied **"New"** (Jauns).
5.  Laukā **Database name** ieraksti nosaukumu, piemēram, `skola`.
6.  Spied pogu **"Create"**.

### 2.2. SQL koda ievietošana no Word dokumenta
Šis solis ir nepieciešams, lai automātiski izveidotu tabulas un aizpildītu tās ar paraugu datiem.

1.  Atver failu `db students.docx`.
2.  Nokopē pirmo daļu — SQL kodu zem sadaļas **"SQL: CREATE TABLE"** (students, teachers, courses, enrollments).
3.  phpMyAdmin vidē, augšējā izvēlnē, izvēlies cilni **"SQL"**.
4.  Ielīmē nokopēto kodu un spied pogu **"Go"** (Izpildīt).
5.  Atkārto to pašu ar kodu sadaļā **"SQL tabulu aizpilde"** (INSERT INTO...), lai datubāzē parādītos informācija.

> **Kāpēc tas jādara?** SQL kods ir instrukcija datubāzei. `CREATE TABLE` izveido tukšu "skapi" datiem, bet `INSERT INTO` ievieto "drēbes" jeb datus šajā skapī.

---

## 3. PHP koda izmantošana

Lai datus no datubāzes attēlotu glītā tabulā mājaslapā, izmanto PHP kodu no Word dokumenta.

1.  Dodies uz mapi `C:\wamp64\www`.
2.  Izveido jaunu mapi, piemēram, `student_checker`.
3.  Izveido jaunu failu `index.php` un atver to ar kodu redaktoru (piem., Notepad++, VS Code).
4.  Nokopē PHP kodu no Word dokumenta (sākot ar `<?php` un beidzot ar tabulas izvadi).
5.  **Svarīgi:** Pārliecinies, ka datubāzes pieslēguma rindā ( `$conn = new mysqli(...)` ) datubāzes nosaukums sakrīt ar to, ko izveidoji phpMyAdmin (piemēram, `test`).
6.  Saglabā failu un pārlūkprogrammā atver `student_checker`.

---

## 4. Mācību procesa soļi (Ieteikums skolotājam)

1.  **Teorija:** Izmanto PDF prezentāciju, lai izskaidrotu, kāpēc datiem jābūt sakārtotiem (normalizētiem).
2.  **Praktiskais Excel:** Ļauj skolēniem patstāvīgi mēģināt sadalīt datus Excel tabulās.
3.  **Realizācija:** Parādi, kā teorētiskā tabula pārtop par īstu datubāzi WampServer vidē, izmantojot SQL kodu.
4.  **Pārbaude:** Izmanto PHP skriptu, lai vizualizētu, ka dati est veiksmīgi sasaistīti.
5.  **Atgriezeniskā saite:** Stundas beigās izmanto "Refleksija" attēlu diskusijai.


---
*Materiālus sagatavoja: Daniels Mēters un Sofia Lucenko (2026)*
