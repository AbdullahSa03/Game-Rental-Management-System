# 🎮 Game Rental Management System  
*A Database Systems Project (CMP 320 – Spring 2024)*

## 👥 Team Members
| Name | ID |
|------|------|
| Mustafa Alani | b00093659 |
| Mohamad Chehab | b00090578 |
| Abdullah Salmeh | b00093434 |

**Section 2**  
**Instructor:** —  

---

# 📌 Project Overview

The **Game Rental Management System** is a full-featured database application designed to manage the renting and returning of video game copies across multiple store branches.  

The system enables both **administrators** and **customer users** to perform operations on branches, games, developers, publishers, customers, and game copies.

This project demonstrates core database concepts including **ER modeling**, **SQL Data Definition**, **SQL DML operations**, **referential integrity**, **constraints**, and **user access control**.

---

# 🗂️ Features

### ✔ **Administrator**
- Add / Update / Delete:
  - Branches
  - Games
  - Publishers
  - Developers
  - Customers
  - Game Copies (per branch)
- Manage system users  
- View all rentals and returns  
- Full DML access

---

### ✔ **Customer User**
- Rent a game copy  
- Return rented games  
- Search games by title, developer, or branch  
- View all available games  
- View rental history  

Passwords are protected using a **modified Caesar cipher encryption** method.

---

# 🧬 ER Diagram Summary

The ER model contains the following relationships:

- **Developer ↔ Game**  
  - Many-to-many  
  - Implemented through an associative table
  
- **Publisher → Game**  
  - One-to-many  

- **Customer ↔ Game Copy**  
  - Many-to-many  
  - GameCopy is a **weak entity**, identified by:  
    - Game ID  
    - Branch ID  
    - Copy Number  

- **Branch → Game Copy**  
  - One-to-many

This structure allows the system to track every individual physical copy of a game and which branch owns it.

---
