# PeerSync — Connect, Collaborate, Succeed 🚀

**PeerSync** is a desktop-based peer-matching and project team management application designed specifically for university students. Inspired by modern social matching interfaces, it addresses common academic team-formation issues—such as communication gaps, unbalanced workloads, and a lack of accountability—by providing a structured, data-driven system where students can find compatible teammates based on skills, work styles, and peer reputations.

Developed as the final term project for **CSC2210: Object Oriented Programming 2 (Spring 2025-2026)** at the *American International University-Bangladesh (AIUB)*.

---

## 👥 Authors (Group 02 - Section A)
* **Sajal Mollick** (ID: 22-49653-3)
* **Md. Azraful Alam** (ID: 24-57476-2)
* **Azizul Alam** (ID: 22-47521-2)
* **Sabrina Islam Shorna** (ID: 22-49569-3)
* **Supervisor:** Tofayet Sultan

---

## ✨ Key Features

### 🔹 Student Features
* **AIUB Student Verification:** Enforces a unique student ID constraint upon registration to filter out unauthorized accounts and restrict platform access to verified peers.
* **Mutual Swipe-Based Matching:** Students browse candidates on a dynamic Home Feed, swiping to connect or pass. A connection is established *only* when both students mutually choose to connect.
* **Skill & Work Style Tagging:** Users customize their profiles by adding programming languages (e.g., C#, Java, C++, Python) and scheduling choices (e.g., Day/Night preference).
* **Project Group Management:** Matched users can collaboratively create atomic project groups bound to specific courses and unique project titles.
* **Reputation & Anonymous Peer Ratings:** Once a project concludes, teammates evaluate one another anonymously across 4 core dimensions: *Contribution, Communication, Reliability, and Punctuality*. 
* **Dynamic Reputation Scores:** An aggregated performance rating is visibly calculated from historic feedback, establishing trust and accountability before groups are finalized.

### 🔸 Administrator Features
* **Centralized Data Surveillance:** Complete visibility of student user records, tracking metrics, and interaction parameters.
* **Full Data Lifecycle CRUD:** Search, add, edit, or remove entries safely using secure, cascading multi-table transactions.

---

## 🛠️ Technical Architecture

* **Frontend UI Framework:** C# .NET Windows Forms (Rich GUI Desktop Environment).
* **Database Management System:** Microsoft SQL Server Express.
* **Data Access Layer:** ADO.NET (`SqlConnection`, `SqlCommand`, `SqlTransaction`, `SqlDataAdapter`).
* **Architecture Pattern:** Two-Tier Desktop Application with secure database transaction isolation boundaries.

---

## 💾 Database Schema & Structure

The underlying relational structure is heavily optimized following **Third Normal Form (3NF)** rules to maintain referential data integrity and eliminate transitive redundancies. 

The system maps properties across **8 primary tables**:
1. `USER` - Stores core credentials, unique AIUB IDs, roles, and reputation tracking scores.
2. `SKILL` - Handles multi-skill references mapped to specific user IDs.
3. `WORK_STYLE` - Stores individual scheduling preferences and working constraints.
4. `SWIPE` - Tracks swiper/swiped choices and timestamps (`IsInterested` Bit flag).
5. `MATCH` - Pairs generated through mutual interaction timestamps.
6. `PROJECT_GROUP` - Group meta logs documenting project instances.
7. `GROUP_MEMBER` - Relational mapping tying members and specific group roles.
8. `RATING` - Multi-dimensional peer breakdown records.

---

## 🚀 Getting Started

### Prerequisites
* Microsoft Visual Studio (2019 / 2022 recommended) with the **.NET Desktop Development** workload installed.
* Microsoft SQL Server & SQL Server Management Studio (SSMS).

### Database Setup
1. Open SQL Server Management Studio (SSMS) and connect to your local server engine instance.
2. Create a new database named `PeerSync`.
3. Execute your normalization DDL scripts to structure the tables (`USER`, `SKILL`, etc.).

### Configuration & Installation
1. Clone this repository locally:
   ```bash
   git clone [https://github.com/CY4NAD3/C-_project_final_term_v.2.4.git](https://github.com/CY4NAD3/C-_project_final_term_v.2.4.git)
