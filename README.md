<!--
  README ini bertema "database": profil = skema, skill = tabel, perjalanan = migrasi.
  Semua diagram memakai Mermaid, yang dirender langsung oleh GitHub (tanpa server pihak ketiga).
  Ganti semua yang bertanda TODO dengan data aslimu.
-->

```sql
-- connected to: github.com/Marst313
-- server: Surakarta, Central Java, Indonesia (UTC+7)

SELECT name, role, status
FROM   developers
WHERE  username = 'Marst313';
```

| name | role | status |
|---|---|---|
| **I Nyoman Karma Dharma Nalendra Wardana** | Junior Software Engineer | `ACTIVE` — open to collaboration |

```
(1 row returned in 0.313 ms)
```

---

### `\d nyoman` — describe schema

Saya membangun aplikasi web dari ujung ke ujung: antarmuka dengan **TypeScript + React**, API dengan **Node.js / Laravel**, dan yang paling saya nikmati, **mendesain struktur data di baliknya**. Kalau ada tabel yang dinormalisasi dengan rapi, saya senang. Kalau ada query yang lambat, saya penasaran.

```mermaid
erDiagram
    NYOMAN ||--o{ LANGUAGE : writes
    NYOMAN ||--o{ PROJECT : ships
    NYOMAN ||--o{ LEARNING : studies
    PROJECT }o--|{ LANGUAGE : "built with"
    PROJECT }o--o| DATABASE : "persists to"

    NYOMAN {
        string role "Junior Software Engineer"
        string base "Surakarta, ID"
        string fuel "coffee"
        boolean open_to_work "true"
    }
    LANGUAGE {
        string typescript "daily driver"
        string javascript "daily driver"
        string php "Laravel"
        string golang "learning"
    }
    DATABASE {
        string postgresql "relational"
        string mysql "relational"
        string mongodb "document"
    }
    LEARNING {
        string nextjs "in progress"
        string graphql "in progress"
        string react_patterns "in progress"
    }
```

---

### `SELECT * FROM stack ORDER BY daily_use DESC;`

| layer | tools |
|---|---|
| `frontend` | ![TypeScript](https://img.shields.io/badge/-TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white) ![React](https://img.shields.io/badge/-React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![Redux](https://img.shields.io/badge/-Redux-593D88?style=flat-square&logo=redux&logoColor=white) ![Tailwind](https://img.shields.io/badge/-Tailwind-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white) ![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) |
| `backend` | ![Node.js](https://img.shields.io/badge/-Node.js-43853D?style=flat-square&logo=node.js&logoColor=white) ![Express](https://img.shields.io/badge/-Express-404D59?style=flat-square&logo=express&logoColor=white) ![Laravel](https://img.shields.io/badge/-Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white) ![Go](https://img.shields.io/badge/-Go-00ADD8?style=flat-square&logo=go&logoColor=white) |
| `database` | ![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white) ![MySQL](https://img.shields.io/badge/-MySQL-005C84?style=flat-square&logo=mysql&logoColor=white) ![MongoDB](https://img.shields.io/badge/-MongoDB-4EA94B?style=flat-square&logo=mongodb&logoColor=white) |
| `infra` | ![AWS](https://img.shields.io/badge/-AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white) ![Vercel](https://img.shields.io/badge/-Vercel-000000?style=flat-square&logo=vercel&logoColor=white) ![Git](https://img.shields.io/badge/-Git-E44C30?style=flat-square&logo=git&logoColor=white) ![Postman](https://img.shields.io/badge/-Postman-FF6C37?style=flat-square&logo=postman&logoColor=white) |

---

### `SELECT * FROM projects WHERE featured = true;`

<!-- TODO: ganti 3 baris ini dengan proyek aslimu. Satu kalimat masalah + satu kalimat hasil lebih kuat dari daftar fitur. -->

| project | what it solves | stack | link |
|---|---|---|---|
| **TODO-nama-proyek-1** | TODO: masalah apa yang diselesaikan, untuk siapa | `React` `TS` `PostgreSQL` | [repo](https://github.com/Marst313/TODO) · [live](https://TODO) |
| **TODO-nama-proyek-2** | TODO | `Laravel` `MySQL` | [repo](https://github.com/Marst313/TODO) |
| **inyomandharma.vercel.app** | Portofolio pribadi saya | `React` `Vercel` | [live](https://inyomandharma.vercel.app/) |

---

### `SELECT * FROM schema_migrations;` — learning journey

```mermaid
timeline
    title Migrations applied to nyoman_db
    001_init : HTML, CSS, JavaScript
    002_add_frontend : React, Redux, Tailwind
    003_add_backend : Node.js, Express, Laravel
    004_add_typescript : TypeScript as daily driver
    005_pending : Next.js, GraphQL, Go
```

<details>
<summary><code>EXPLAIN ANALYZE</code> — courses</summary>

<br>

| course | status |
|---|---|
| JavaScript: From Zero to Mastery | `COMMITTED` |
| React – The Complete Guide | `IN TRANSACTION` |
| Node.js Developer Course | `IN TRANSACTION` |

</details>

---

### `SELECT stats FROM github;`

<div align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=Marst313&show_icons=true&hide_border=true&count_private=true&theme=transparent&title_color=336791&icon_color=336791" alt="GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Marst313&layout=compact&hide_border=true&langs_count=6&theme=transparent&title_color=336791" alt="Top languages" />
</div>

---

### `INSERT INTO conversations (you, me) VALUES (?, ?);`

```sql
-- pilih koneksi favoritmu:
```

[![Portfolio](https://img.shields.io/badge/-Portfolio-336791?style=flat-square&logo=google-chrome&logoColor=white)](https://inyomandharma.vercel.app/)
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/i-nyoman-karma-dharma-nalendra-wardana/)
[![Email](https://img.shields.io/badge/-dlegoinyoman1@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:dlegoinyoman1@gmail.com)
[![Instagram](https://img.shields.io/badge/-@inyoman__dharma-E4405F?style=flat-square&logo=instagram&logoColor=white)](https://www.instagram.com/inyoman_dharma/)

```
COMMIT;  -- terima kasih sudah mampir ☕
```
