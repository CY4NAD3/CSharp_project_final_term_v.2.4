# PeerSync — Connect, Collaborate, Succeed 🚀

[cite_start]**PeerSync** is a desktop-based peer-matching and project team management application designed specifically for university students[cite: 151, 154]. [cite_start]Inspired by modern social matching interfaces, it addresses common academic team-formation issues—such as communication gaps, unbalanced workloads, and lack of accountability—by providing a structured, data-driven system where students can find compatible teammates based on skills, work styles, and peer reputations[cite: 156, 157, 158, 159].

[cite_start]Developed as the final term project for **CSC2210: Object Oriented Programming 2 (Spring 2025-2026)** at the *American International University-Bangladesh (AIUB)*[cite: 137, 139, 140].

---

## 👥 Authors (Group 02 - Section A)
* [cite_start]**Sajal Mollick** (ID: 22-49653-3) [cite: 141, 142, 149]
* [cite_start]**Azraful Alam** (ID: 24-57476-2) [cite: 149]
* [cite_start]**Azizul Alam** (ID: 22-47521-2) [cite: 149]
* [cite_start]**Sabrina Islam Shorna** (ID: 22-49569-3) [cite: 149]
* [cite_start]**Supervisor:** Tofayet Sultan [cite: 148]

---

## ✨ Key Features

### 🔹 Student Features
* [cite_start]**AIUB Student Verification:** Enforces a unique student ID constraint upon registration to filter out fake accounts and restrict platform access to verified peers[cite: 268, 270].
* [cite_start]**Mutual Swipe-Based Matching:** Students browse candidates on a dynamic Home Feed, swiping to connect or pass[cite: 266]. [cite_start]A connection is established *only* when both students mutually choose to connect[cite: 267].
* [cite_start]**Skill & Work Style Tagging:** Users customize their profiles by adding programming languages (e.g., C#, Java, C++) and scheduling choices (e.g., Day/Night preference)[cite: 165, 245, 247].
* [cite_start]**Project Group Management:** Matched users can collaboratively create atomic project groups bound to specific courses and unique project titles[cite: 278, 279].
* [cite_start]**Reputation & Anonymous Peer Ratings:** Once a project concludes, teammates evaluate one another anonymously across 4 core dimensions: *Contribution, Communication, Reliability, and Punctuality*[cite: 271, 272]. 
* [cite_start]**Dynamic Reputation Scores:** An aggregated performance rating is visibly calculated from historic feedback, establishing trust and accountability before groups are finalized[cite: 274, 275, 276].

### 🔸 Administrator Features
* [cite_start]**Centralized Data surveillance:** Complete visibility of student user records, tracking metrics, and interaction parameters[cite: 116, 280, 281].
* [cite_start]**Full Data Lifecycle CRUD:** Search, add, edit, or remove entries safely using secure, cascading multi-table transactions[cite: 281, 282].

---

## 🛠️ Technical Architecture

* [cite_start]**Frontend UI Framework:** C# .NET Windows Forms (Rich GUI Desktop Environment)[cite: 151, 163, 171].
* [cite_start]**Database Management System:** Microsoft SQL Server Express[cite: 78, 163].
* [cite_start]**Data Access Layer:** ADO.NET (`SqlConnection`, `SqlCommand`, `SqlTransaction`, `SqlDataAdapter`)[cite: 75, 85].
* [cite_start]**Architecture Pattern:** Two-Tier Desktop Application with secure database transaction isolation boundaries[cite: 63, 65, 151].

---

## 💾 Database Schema & Structure

[cite_start]The underlying relational structure is heavily optimized following **Third Normal Form (3NF)** rules to maintain referential data integrity and eliminate transitive redundancies[cite: 167, 218, 220]. 

[cite_start]The system maps properties across **8 primary tables**[cite: 174, 238]:
1. [cite_start]`USER` - Stores core credentials, unique AIUB IDs, roles, and reputation tracking scores[cite: 221, 270].
2. [cite_start]`SKILL` - Handles multi-skill references mapped to specific user IDs[cite: 223].
3. [cite_start]`WORK_STYLE` - Stores individual scheduling preferences and working constraints[cite: 225].
4. [cite_start]`SWIPE` - Tracks swiper/swiped choices and timestamps (`IsInterested` Bit flag)[cite: 227].
5. [cite_start]`MATCH` - Pairs generated through mutual interaction timestamps[cite: 229, 267].
6. [cite_start]`PROJECT_GROUP` - Group meta logs documenting project instances[cite: 231].
7. [cite_start]`GROUP_MEMBER` - Relational mapping tying members and specific group roles[cite: 233].
8. [cite_start]`RATING` - Multi-dimensional peer breakdown records[cite: 235].

---

## 🚀 Getting Started

### Prerequisites
* Microsoft Visual Studio (2019 / 2022 recommended) with **.NET Desktop Development** workload installed.
* Microsoft SQL Server & SQL Server Management Studio (SSMS).

### Database Setup
1. [cite_start]Open SQL Server Management Studio (SSMS) and connect to your local server engine instance[cite: 78].
2. Create a new database named `PeerSync`.
3. [cite_start]Execute your normalization DDL scripts to structure the tables (`USER`, `SKILL`, etc.)[cite: 174, 218].

### Configuration & Installation
1. Clone this repository locally:
   ```bash
   git clone [https://github.com/CY4NAD3/C-_project_final_term_v.2.4.git](https://github.com/CY4NAD3/C-_project_final_term_v.2.4.git)
