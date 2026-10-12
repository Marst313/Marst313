<!--
  Theme: profile as a database.
  All diagrams use Mermaid, rendered natively by GitHub (no third-party servers).
  Rows marked TODO: fill in from your portfolio before committing.
-->

```sql
-- connected to github.com/Marst313
-- server: Indonesia (UTC+7)

SELECT name, role, experience, status
FROM   developers
WHERE  username = 'Marst313';
```

| name | role | experience | status |
|---|---|---|---|
| **I Nyoman Karma Dharma Nalendra Wardana** | Fullstack Developer · JS/TS · Go · Odoo | `2+ years` | `OPEN_TO_COLLABORATE` |

```
(1 row returned in 0.313 ms)
```

---

### `\d nyoman` · describe schema

I build web and mobile apps end to end: interfaces with **React, React Native and Next.js**, APIs with **Node.js** and lately **Go**, and business modules in **Odoo (Python)**. What I enjoy most is the layer underneath — schemas, migrations, auth, and the pipeline that ships it all.

```mermaid
erDiagram
    NYOMAN ||--o{ SKILL : masters
    NYOMAN ||--o{ PROJECT : ships
    NYOMAN ||--o{ LEARNING : studies
    PROJECT }o--|{ SKILL : "built with"
    PROJECT }o--o| DATABASE : "persists to"

    NYOMAN {
        string role "Fullstack Developer"
        string degree "B.CS, GPA 3.83"
        int years_exp "2+"
        string award "1st place software dev competition"
    }
    SKILL {
        string frontend "React, Next.js, TypeScript"
        string mobile "React Native"
        string backend "Node.js, Express, Go, Laravel"
        string erp "Odoo, Python, XML"
    }
    DATABASE {
        string postgresql "relational"
        string mysql "relational"
        string mongodb "document"
    }
    LEARNING {
        string golang "Gin, JWT, migrations"
        string devops "Docker, GitHub Actions"
        string architecture "clean architecture"
    }
```

---

### `SELECT * FROM skills ORDER BY daily_use DESC;`

| layer | tools | what I do with them |
|---|---|---|
| `frontend` | ![TypeScript](https://img.shields.io/badge/-TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white) ![React](https://img.shields.io/badge/-React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![Next.js](https://img.shields.io/badge/-Next.js-000000?style=flat-square&logo=next.js&logoColor=white) ![Redux](https://img.shields.io/badge/-Redux-593D88?style=flat-square&logo=redux&logoColor=white) ![Tailwind](https://img.shields.io/badge/-Tailwind-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white) ![Vue](https://img.shields.io/badge/-Vue.js-35495E?style=flat-square&logo=vue.js&logoColor=4FC08D) | Figma-to-React UIs, reusable typed components, responsive layouts |
| `mobile` | ![React Native](https://img.shields.io/badge/-React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB) | Upgrading legacy apps across major versions (0.63 → 0.79) |
| `backend` | ![Node.js](https://img.shields.io/badge/-Node.js-43853D?style=flat-square&logo=node.js&logoColor=white) ![Express](https://img.shields.io/badge/-Express-404D59?style=flat-square&logo=express&logoColor=white) ![Go](https://img.shields.io/badge/-Go-00ADD8?style=flat-square&logo=go&logoColor=white) ![Gin](https://img.shields.io/badge/-Gin-008ECF?style=flat-square&logo=gin&logoColor=white) ![Laravel](https://img.shields.io/badge/-Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white) | REST APIs, JWT auth, role-based access, microservices |
| `erp` | ![Odoo](https://img.shields.io/badge/-Odoo-714B67?style=flat-square&logo=odoo&logoColor=white) ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) | Custom modules, access-request and approval workflows |
| `database` | ![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white) ![MySQL](https://img.shields.io/badge/-MySQL-005C84?style=flat-square&logo=mysql&logoColor=white) ![MongoDB](https://img.shields.io/badge/-MongoDB-4EA94B?style=flat-square&logo=mongodb&logoColor=white) ![Prisma](https://img.shields.io/badge/-Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white) | Schema design, migrations, query tuning |
| `devops` | ![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/-GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white) ![Vercel](https://img.shields.io/badge/-Vercel-000000?style=flat-square&logo=vercel&logoColor=white) ![Git](https://img.shields.io/badge/-Git-E44C30?style=flat-square&logo=git&logoColor=white) ![Postman](https://img.shields.io/badge/-Postman-FF6C37?style=flat-square&logo=postman&logoColor=white) | Containerized deploys, CI/CD to VPS |

<details>
<summary><code>SELECT concept FROM skills WHERE type = 'practice';</code></summary>

<br>

`REST API design` · `Clean Architecture` · `MVC` · `OOP` · `Role-based access control` · `Unit testing` · `Agile / Scrum` · `Code review`

</details>

---

### `SELECT * FROM projects WHERE featured = true;`

<!-- TODO: add the rest of your portfolio projects here, one row each: name | what it does | stack | links -->

| project | what it does | stack | links |
|---|---|---|---|
| **Reminder API** | Reminder REST API with JWT auth, schema migrations, a cron job that resets completed tasks, unit tests, and CI/CD to a VPS | `Go` `Gin` `PostgreSQL` `Docker` `GitHub Actions` | [code](https://github.com/Marst313/learn-go) |
| **Portfolio** | Personal site with project search and category filters | `Next.js` `Tailwind` `Airtable` | [code](https://github.com/Marst313/portofolio) · [live](https://inyomandharma.vercel.app/) |
| **TODO project name** | TODO one sentence: the problem it solves | `TODO` | [code](https://github.com/Marst313/TODO) · [live](https://TODO) |
| **TODO project name** | TODO | `TODO` | [code](https://github.com/Marst313/TODO) |

---

### `SELECT * FROM schema_migrations;` · learning journey

```mermaid
timeline
    title migrations applied to nyoman_db
    2021 : HTML & CSS : first static site
    2022 : C++ algorithms : lab assistant for 50+ students
    2023 : JavaScript, React, Node.js : 1st place software dev competition
    2024 : Express, MongoDB, ML APIs : Node.js Expert certification
    2025 : TypeScript, Next.js : React Native, microservices
    2026 : Odoo & Python : Go, Gin, JWT, Docker, CI/CD
```

<details>
<summary><code>SELECT * FROM certifications;</code></summary>

<br>

| certification | year |
|---|---|
| Junior Web Developer (Kominfo) | 2023 |
| React 18 Complete Guide (Udemy) | 2023 |
| Cloud Practitioner Essentials (Dicoding) | 2023 |
| Node.js Expert (Udemy) | 2024 |

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
COMMIT;  -- thanks for stopping by ☕
```
