# 🎵 Music Store SQL Analysis

End-to-end SQL analysis on a digital music store database using PostgreSQL, covering customer behavior, sales trends, and genre insights.

---

## 📌 Objective

Answer real business questions using structured SQL queries — from identifying top customers to finding the most popular genre per country.

---

## 🗂️ Files

| File | Description |
|------|-------------|
| `Music_Store_database.sql` | Full database schema & raw data |
| `music_store_analysis.sql` | All analysis queries (Easy → Advanced) |

---

## 🗃️ Database Schema (ERD)

![Music Store Database Schema](MusicDatabaseSchema.png)

The database consists of **11 tables** covering the full music store ecosystem:

- **Employee & Customer**: `employee` links to `customer` (support rep relationship). Customers are tied to invoices.
- **Invoice Flow**: `invoice` → `invoice_line` → `track` captures every purchase transaction.
- **Music Catalog**: `track` belongs to an `album`, which belongs to an `artist`. Each track has a `genre` and `media_type`.
- **Playlist**: `playlist` and `playlist_track` allow tracks to be grouped independently of purchases.

> Key relationships to note: A single customer can have many invoices; each invoice line maps to exactly one track. Genre is at the track level, enabling per-country genre popularity analysis.

---

## 🔍 Questions Answered

### 🟢 Easy
- Senior most employee by job title
- Countries with the most invoices
- Top 3 invoice values
- City with highest total invoice revenue
- Best customer by total spending

### 🟡 Moderate
- Rock music listeners — email list ordered alphabetically
- Top 10 rock artists by track count
- Tracks longer than average song length

### 🔴 Advanced
- Amount spent by each customer per artist (using CTEs)
- Most popular genre per country (CTE + Recursive methods)
- Top spending customer per country (CTE + Recursive methods)

---

## 📸 Sample Outputs

> Screenshots will be added here. Suggested placements:
> - Best customer by total spending<img width="1200" height="600" alt="1" src="https://github.com/user-attachments/assets/6fb4688a-cb1d-4411-9db3-ad565c19f264" />

> - ✅ Easy: City with highest revenue
> - ✅ Moderate: Top 10 rock artists
> - ✅ Advanced: Most popular genre per country (CTE)
> - ✅ Advanced: Top spending customer per country

*Replace the above with actual query result screenshots from pgAdmin / VS Code SQLTools.*

---

## 💡 Key Insights

- **Rock** is the most purchased genre globally
- **Prague** has the highest total invoice revenue
- **USA** dominates in total number of invoices
- CTEs and recursive queries enable clean, readable solutions for complex aggregations across countries

---

## 🛠️ Tools Used

- PostgreSQL
- pgAdmin / VS Code SQLTools
- CTEs, Window Functions, Subqueries, Recursive Queries

---

## 🚀 How to Run

1. Clone the repo
2. Open `Music_Store_database.sql` in pgAdmin and run it to set up the database
3. Open `music_store_analysis.sql` and run queries individually or all at once

---

## 👤 Author

[Shreyash Mandlik](https://github.com/shreyash-mandlik)
