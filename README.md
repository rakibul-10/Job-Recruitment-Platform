
## Project Title
**Job Recruitment Platform**

Tech Titans is a complete **Job Recruitment System** where **Job Seekers, Employers, and Admins** collaborate seamlessly.  
The system mainly focuses on **Job Posting, Application Management, User Role Management, Company Profiles, and Category-wise Jobs**.  

---

## 📌 ER Diagram Overview  

The core entities of the system are:  

- **User** → Represents all accounts (Admin, Job Seeker, Employer).  
- **Employees** → Stores company details associated with employers.  
- **Jobs** → Job postings created by employers.  
- **Job Categories** → Classification of jobs (e.g., IT, Finance, Marketing).  
- **Job Applications** → Applications submitted by job seekers for jobs.  

### 🔗 Relationship Summary  

- A **User** can be an **Admin, Job Seeker, or Employer**.  
- An **Employer (User)** is linked with a **Company (Employees)**.  
- **Jobs** are created by Employers and fall under a **Job Category**.  
- **Job Applications** connect **Job Seekers (Users)** with **Jobs**.  

---

## 🚀 Key Features  

### 👤 Job Seeker Features  
- Register and log in.  
- Manage personal profile.  
- Browse and search jobs.  
- Apply for jobs.  
- Track application status.  

### 🏢 Employer Features  
- Create company profile.  
- Post new jobs.  
- View submitted applications.  
- Update application status.  

### 🛠️ Admin Features  
- Manage users and assign roles.  
- Monitor jobs and applications.  
- Oversee overall system workflow and data.  

---

## 📂 Database Schema  

### 1. **User Table**  
- `id (PK)`  
- `email`  
- `password`  
- `role` (Admin / Job Seeker / Employer)  
- `username`  

### 2. **Employees Table**  
- `id (PK)`  
- `company_name`  
- `description`  
- `user_id (FK → User.id)`  

### 3. **Jobs Table**  
- `id (PK)`  
- `title`  
- `description`  
- `category_id (FK → Job_Categories.id)`  
- `company_id (FK → Employees.id)`  

### 4. **Job Categories Table**  
- `id (PK)`  
- `name`  

### 5. **Job Applications Table**  
- `id (PK)`  
- `application_date`  
- `status`  
- `job_id (FK → Jobs.id)`  
- `job_seeker_id (FK → User.id)`  

---

## Getting Started  
1. Clone the repository
2. Install dependencies
3. Start development

---
## Development Guidelines

1. Create feature branches
2. Make small, focused commits
3. Write descriptive commit messages
4. Create pull requests for review
---
## Resources

[1.Project Documentation]( )  
[2.Development Setup]()  
[3.Contributing Guidelines]()
