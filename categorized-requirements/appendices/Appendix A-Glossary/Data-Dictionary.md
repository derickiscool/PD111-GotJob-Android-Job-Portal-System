### User Account
| Field Name | Data Type | Description | Constraints | Example |
| :--- | :--- | :--- | :--- | :--- |
| **FirstName** | String | User’s given name | Not Null | Louis |
| **LastName** | String | User’s surname | Not Null | Tan |
| **Email** | VARCHAR(255) | User’s login email | Unique, Not Null | louis20@gmail.com |
| **PhoneNo** | VARCHAR(20) | User’s contact number | Null allowed | 6590123456 |
| **PasswordHash** | VARCHAR(255) | Secure password storage | Not Null | $2b$12$abc... |
| **Role** | ENUM | Account role | Not Null; (user, recruiter) | user |
| **LastLoginDate** | DateTime | Most recent login timestamp | Not Null, cannot be a future date | 2025-12-01 14:22 |
| **ProfileStatus** | Enum | Current account state | Not Null | Active |

### Job Seeker Profile
| Field Name | Data Type | Description | Constraints | Example |
| :--- | :--- | :--- | :--- | :--- |
| **JobSeekerID** | Integer | System-generated unique identifier for a job seeker | Primary Key, Not Null | 123456 |
| **Skills** | String | Professional skills for matching | Null allowed | Java, SQL, Office |
| **YearsOfExperience** | Integer | Total years of professional experience | Not Null | 5 |
| **HighestEducation** | VARCHAR(80) | Highest qualification | Null allowed | Diploma |
| **Location** | VARCHAR(120) | Preferred work location | Null allowed | Singapore |

### Recruiter Profile
| Field Name | Data Type | Description | Constraints | Example |
| :--- | :--- | :--- | :--- | :--- |
| **RecruiterID** | Integer | System-generated unique identifier for the recruiter | Primary Key, Not Null | 567890 |
| **CompanyName** | VARCHAR(120) | Recruiter organisation name | Not Null | Uwais Hiring Agency |
| **CompanyUEN** | VARCHAR(20) | Company registration number | Null allowed | 20191234Z |
| **TierLevel** | Integer | Access authorization levels | Not Null, must match policy rules | 2 |
| **RelationshipPolicy** | String | Defines profile viewing rights | Not Null, must match SRS authorisation rules | REL-01 |

### Job Posting
| Field Name | Data Type | Description | Constraints | Example |
| :--- | :--- | :--- | :--- | :--- |
| **JobID** | Integer | Unique job identifier | Primary Key, Not Null | 1023 |
| **RecruiterID** | Integer | Job owner | Foreign Key from Recruiter Profile, Not Null | 567890 |
| **JobTitle** | VARCHAR(120) | Title of job posting | Not Null | Software Engineer |
| **JobDescription** | Text | Detailed job description | Not Null | …designs, develops, and maintains scalable software applications, requiring proficiency in programming languages… |
| **RequiredSkills** | String | Skills required for the role | Not Null | Java, Spring, Python, App Development |
| **JobLocation** | VARCHAR(120) | Work location | Not Null | Singapore |
| **EmploymentType** | ENUM | Full-time/part-time job | Not Null; (FT, PT) | FT |
| **Salary** | DECIMAL(10,2) | Salary of the job | Not Null | 8000.00 |
| **PostedDate** | DateTime | Date job posted | Not Null | 2026-01-15 |
| **JobStatus** | Enum | Job availability status | Not Null; (Open, Closed) | Open |

### Job Application
| Field Name | Data Type | Description | Constraints | Example |
| :--- | :--- | :--- | :--- | :--- |
| **ApplicationID** | Integer | Unique application ID | Primary Key, Not Null | 9001 |
| **JobSeekerID** | Integer | Unique identifier for job seeker | Foreign Key from Job Seeker Profile, Not Null | 123456 |
| **JobID** | Integer | Unique job identifier | Foreign Key from Job Posting, Not Null | 1023 |
| **ApplicationDate** | DateTime | Date job posted | Not Null | 2026-01-15 |
| **ApplicationStatus** | Enum | Job availability status | Not Null | Shortlisted |