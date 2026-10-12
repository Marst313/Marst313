<!--
  Tema: profil sebagai database.
  Semua diagram memakai Mermaid, dirender langsung oleh GitHub tanpa server pihak ketiga.
  Baris bertanda TODO: isi dengan link repo yang benar sebelum commit.
-->

```sql
-- connected to github.com/Marst313
-- server: Yogyakarta, Indonesia (UTC+7)

SELECT name, role, current_company, status
FROM   developers
WHERE  username = 'Marst313';
```

| name | role | status |
|---|---|---|---|
| **I Nyoman Karma Dharma Nalendra Wardana** | Fullstack Developer · JS/TS, Go, Odoo | `ACTIVE` |

```
(1 row returned in 0.313 ms)
```

---

### `\d nyoman` · describe schema

Saya membangun aplikasi web dan mobile dari ujung ke ujung: antarmuka dengan **React / React Native / Next.js**, API dengan **Node.js**, dan sekarang **Go**. Di kantor saya menulis modul **Odoo** (Python) untuk alur kerja internal, seperti permintaan akses user dan approval berjenjang. Di luar kantor, saya senang membongkar hal yang ada di balik layar: skema database, migrasi, auth, dan pipeline deploy.

```mermaid
erDiagram
    NYOMAN ||--o{ EXPERIENCE : "worked at"
    NYOMAN ||--o{ PROJECT : ships
    NYOMAN ||--o{ LEARNING : studies
    PROJECT }o--|{ STACK : "built with"
    PROJECT }o--o| DATABASE : "persists to"

    NYOMAN {
        string role "Fullstack Developer"
        string base "Yogyakarta, ID"
        string degree "B.CS Amikom, GPA 3.83"
        int years_exp "2+"
    }
    STACK {
        string daily "TypeScript, React, Node.js"
        string mobile "React Native"
        string work "Odoo, Python, XML"
        string backend "Go, Express, Laravel"
    }
    DATABASE {
        string postgresql "relational"
        string mysql "relational"
        string mongodb "document"
    }
    LEARNING {
        string golang "REST API, Gin, JWT"
        string devops "Docker, GitHub Actions, VPS"
        string architecture "clean architecture"
    }
```

---

### `SELECT * FROM stack ORDER BY daily_use DESC;`

| layer | tools |
|---|---|
| `frontend` | ![TypeScript](https://img.shields.io/badge/-TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white) ![React](https://img.shields.io/badge/-React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![Next.js](https://img.shields.io/badge/-Next.js-000000?style=flat-square&logo=next.js&logoColor=white) ![Redux](https://img.shields.io/badge/-Redux-593D88?style=flat-square&logo=redux&logoColor=white) ![Tailwind](https://img.shields.io/badge/-Tailwind-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white) ![Vue](https://img.shields.io/badge/-Vue.js-35495E?style=flat-square&logo=vue.js&logoColor=4FC08D) |
| `mobile` | ![React Native](https://img.shields.io/badge/-React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB) |
| `backend` | ![Node.js](https://img.shields.io/badge/-Node.js-43853D?style=flat-square&logo=node.js&logoColor=white) ![Express](https://img.shields.io/badge/-Express-404D59?style=flat-square&logo=express&logoColor=white) ![Go](https://img.shields.io/badge/-Go-00ADD8?style=flat-square&logo=go&logoColor=white) ![Gin](https://img.shields.io/badge/-Gin-008ECF?style=flat-square&logo=gin&logoColor=white) ![Laravel](https://img.shields.io/badge/-Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white) |
| `erp` | ![Odoo](https://img.shields.io/badge/-Odoo-714B67?style=flat-square&logo=odoo&logoColor=white) ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) |
| `database` | ![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white) ![MySQL](https://img.shields.io/badge/-MySQL-005C84?style=flat-square&logo=mysql&logoColor=white) ![MongoDB](https://img.shields.io/badge/-MongoDB-4EA94B?style=flat-square&logo=mongodb&logoColor=white) ![Prisma](https://img.shields.io/badge/-Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white) |
| `devops` | ![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/-GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white) ![Vercel](https://img.shields.io/badge/-Vercel-000000?style=flat-square&logo=vercel&logoColor=white) ![Git](https://img.shields.io/badge/-Git-E44C30?style=flat-square&logo=git&logoColor=white) ![Postman](https://img.shields.io/badge/-Postman-FF6C37?style=flat-square&logo=postman&logoColor=white) |

---

### `SELECT * FROM employment ORDER BY started_at;`

```mermaid
gantt
    title employment + education
    dateFormat YYYY-MM
    axisFormat %Y
    section Education
    Amikom University, Computer Science       :done, 2021-09, 2025-06
    section Experience
    Kampus Merdeka Independent Study          :done, 2023-08, 2023-12
    Polda DIY, case tracking app              :done, 2023-12, 2024-02
    Kampus Merdeka Web Dev Internship         :done, 2024-09, 2024-12
    Widya Matador, Fullstack Intern           :done, 2025-02, 2025-04
    Aksamedia, Front End Intern               :done, 2025-02, 2025-06
    Sieben Technology, Software Engineer      :done, 2025-07, 2025-11
    Flexypack, Fullstack and Odoo Developer   :active, 2025-12, 2026-10
```

<details>
<summary><code>SELECT company, highlight FROM employment;</code></summary>

<br>

| company | role | highlight |
|---|---|---|
| **Flexypack** · Yogyakarta | Fullstack & Odoo Developer | Modul Odoo kustom; fitur *Request Access User* dengan approval workflow untuk izin menu dan modul |
| **Sieben Technology** · remote | Software Engineer | Upgrade React Native dari v0.63 ke v0.79; fitur di arsitektur microservices |
| **Aksamedia** · remote | Front End Intern | Desain Figma menjadi UI React responsif; integrasi REST API |
| **Widya Matador** · remote | Fullstack Intern | Komponen React + TypeScript; API dan dokumentasi untuk produk IoT |
| **Kampus Merdeka** (Infinite Learning) | Web Dev Intern | Aplikasi peringkas teks berbasis ML: Node.js, Express, MongoDB, RBAC |
| **Reskrimsus Polda DIY** | Developer | Aplikasi pelacakan kasus internal dan dashboard analitik |

</details>

---

### `SELECT * FROM projects WHERE featured = true;`

| project | what it does | stack | link |
|---|---|---|---|
| **Reminder API** | REST API pengingat dengan auth JWT, migrasi skema, cron job yang mereset tugas selesai, unit test, dan CI/CD ke VPS | `Go` `Gin` `PostgreSQL` `Docker` `GitHub Actions` | [repo](https://github.com/Marst313/learn-go) |
| **Portfolio** | Situs portofolio dengan filter dan pencarian proyek | `Next.js` `Tailwind` `Airtable` | [repo](https://github.com/Marst313/portofolio) · [live](https://inyomandharma.vercel.app/) |
| **ML Text Summarizer** | Aplikasi peringkas teks dengan integrasi model ML dan role-based access | `React` `Node.js` `Express` `MongoDB` | <!-- TODO --> [repo](https://github.com/Marst313/TODO) |
| **Child Growth Monitor** 🥇 | Juara 1 Ignation Software Development Competition: memantau tumbuh kembang anak | `React` `Node.js` | <!-- TODO --> [repo](https://github.com/Marst313/TODO) |

---

### `SELECT * FROM schema_migrations;` · learning journey

```mermaid
timeline
    title migrations applied to nyoman_db
    2021 : HTML & CSS : first static portfolio
    2022 : C++ algorithms : lab assistant for 50+ students
    2023 : JavaScript, React, Node.js : Kampus Merdeka independent study : 1st place Ignation
    2024 : Express, MongoDB, ML APIs : Node.js Expert cert
    2025 : TypeScript, Next.js : React Native, microservices
    2026 : Odoo & Python at work : Go, Gin, JWT, Docker, CI/CD
```

<details>
<summary><code>SELECT * FROM certifications;</code></summary>

<br>

| certification | issuer | year |
|---|---|---|
| Junior Web Developer | Kominfo | 2023 |
| React 18 Complete Guide | Udemy | 2023 |
| Cloud Practitioner Essentials | Dicoding | 2023 |
| Node.js Expert | Udemy | 2024 |

</details>

---

### `SELECT stats FROM github;`

<div align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=Marst313&show_icons=true&hide_border=true&count_private=true&theme=transparent&title_color=336791&icon_color=336791" alt="GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Marst313&layout=compact&hide_border=true&langs_count=6&theme=transparent&title_color=336791" alt="Top languages" />
</div>

---

### `INSERT INTO conversations (you, me) VALUES (?, ?);`

[![Portfolio](https://img.shields.io/badge/-Portfolio-336791?style=flat-square&logo=google-chrome&logoColor=white)](https://inyomandharma.vercel.app/)
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/i-nyoman-karma-dharma-nalendra-wardana/)
[![Email](https://img.shields.io/badge/-dlegoinyoman1@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:dlegoinyoman1@gmail.com)
[![Instagram](https://img.shields.io/badge/-@inyoman__dharma-E4405F?style=flat-square&logo=instagram&logoColor=white)](https://www.instagram.com/inyoman_dharma/)

```
COMMIT;  -- terima kasih sudah mampir ☕
```
