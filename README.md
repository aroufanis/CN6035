# Εφαρμογή Κρατήσεων Θέσεων σε Εστιατόριο (CN6035 - 2025)

Αυτή η εφαρμογή επιτρέπει σε χρήστες να εγγραφούν, να συνδεθούν, να δουν διαθέσιμα εστιατόρια και να κάνουν κρατήσεις τραπεζιών μέσω κινητής συσκευής.

## Δομή Αποθετηρίου

roufanis/
├── api/ # Node.js backend (Express.js)
│ ├── src/
│ │ ├── routes/ # API routes
│ │ ├── controllers/ # Επιχειρησιακή λογική
│ │ ├── models/ # Διασύνδεση DB
│ │ └── app.js # Εγκατάσταση Express και middleware
│ ├── .env.* # Ρυθμίσεις για κάθε περιβάλλον
│ ├── package.json
│ └── server.js
├── eroufanis22b_db1.sql # SQL dump για MariaDB

yaml


---

## Οδηγίες Εγκατάστασης

### 1. Κλωνοποίηση Αποθετηρίου

```bash
git clone https://gitlab.com/username/restaurant-reservation-app.git
cd restaurant-reservation-app/roufanis/api

Εγκατάσταση Εξαρτήσεων

npm install

Ρύθμιση Περιβάλλοντος

Δημιουργήστε αρχείο .env (ή χρησιμοποιήστε .env.development) με μεταβλητές:

PORT=3000
DB_HOST=localhost
DB_PORT=3306
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=restaurant_app
JWT_SECRET=your_jwt_secret

Εκκίνηση Backend

npm start

Δοκιμές API με Postman

Παραδείγματα endpoints:

    POST /register – Εγγραφή χρήστη

    POST /login – Επιστροφή JWT

    GET /restaurants – Λίστα εστιατορίων

    POST /reservations – Νέα κράτηση

Εγκατάσταση Βάσης Δεδομένων (MariaDB)
SQL
CREATE DATABASE restaurant_app;

Εισαγωγή SQL Dump:

mysql -u root -p restaurant_app < eroufanis22b_db1.sql

Τεχνολογίες

    Backend: Node.js + Express

    Βάση: MariaDB

    Authentication: JWT

    Tooling: Postman, GitLab, NetBeans

Κατάσταση Υλοποίησης

Backend API (register, login, reservations)

Σύνδεση με MariaDB

Frontend (React Native – σε ξεχωριστό φάκελο, προαιρετικό)

Άδεια

Εκπαιδευτικό έργο για το μάθημα Mobile & Distributed Systems – CN6035
