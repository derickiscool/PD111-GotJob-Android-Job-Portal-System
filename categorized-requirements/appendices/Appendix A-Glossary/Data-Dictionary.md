### UserAccount (Shared Login Identity)
| Field Name | Data Type | Description | Constraints | Example |
| :--- | :--- | :--- | :--- | :--- |
| **FirstName** | String | User’s given name | Not Null | Louis |
| **LastName** | String | User’s surname | Null allowed | Tan |
| **Email** | Varchar(255) | User’s login email | Unique, Not Null | louis20@gmail.com |
| **PhoneNo** | Varchar(20) | User’s contact number | Null allowed | 6590123456 |
| **PasswordHash** | Varchar(255) | Secure password storage | Not Null | $2b$12$abc... |
| **Role** | Enum | Account role | Not Null; (user, recruiter) | user |
| **LastLoginDate** | DateTime | Most recent login timestamp | Not Null | 2025-12-01 14:22 |
| **ProfileStatus** | Enum | Current account state | Not Null | Active |

### JobSeekerProfile
| Field Name | Data Type | Description | Constraints | Example |
| :--- | :--- | :--- | :--- | :--- |
| **JobSeekerID** | Integer | System-generated unique identifier for a job seeker | Primary Key, Not Null | 123456 |
| **Skills** | Text | Professional skills for matching | Null allowed | Java, SQL, Office |
| **YearsOfExperience** | Integer | Total years of professional experience | Null allowed | 5 |
| **HighestEducation** | Varchar(80) | Highest qualification | Null allowed | Diploma |
| **Location** | Varchar(120) | Preferred work location | Null allowed | Singapore |

### RecruiterProfile
| Field Name | Data Type | Description | Constraints | Example |
| :--- | :--- | :--- | :--- | :--- |
| **RecruiterID** | Integer | System-generated unique identifier for the recruiter | Primary Key, Not Null | 567890 |
| **CompanyName** | Varchar(120) | Recruiter organisation name | Not Null | Uwais Hiring Agency |
| **CompanyUEN** | Varchar(20) | Company registration number | Null allowed | 20191234Z |
| **TierLevel** | Integer | Access authorization levels | Not Null, must match policy rules | 2 |
| **RelationshipPolicy** | String | Defines profile viewing rights | Not Null, must match SRS authorisation rules | REL-01 |

### JobPosting
| Field Name | Data Type | Description | Constraints | Example |
| :--- | :--- | :--- | :--- | :--- |
| **JobID** | Integer | Unique job identifier | Primary Key, Not Null | 1023 |
| **RecruiterID** | Integer | Job owner | Foreign Key from RecruiterProfile, Not Null | 567890 |
| **JobTitle** | Varchar(120) | Title of job posting | Not Null | Software Engineer |
| **JobDescription** | Text | Detailed job description | Not Null | …designs, develops, and maintains scalable software applications, requiring proficiency in programming languages… |
| **RequiredSkills** | String | Skills required for the role | Not Null | Java, Spring, Python, App Development |
| **JobLocation** | Varchar(120) | Work location | Not Null | Singapore |
| **EmploymentType** | Enum | Full-time/part-time job | Not Null; (FT, PT) | FT |
| **Salary** | Decimal(10,2) | Salary of the job | Null allowed | 8000.00 |
| **PostedDate** | DateTime | Date job posted | Not Null | 2026-01-15 12:31 |
| **JobStatus** | Enum | Job availability status | Not Null; (Open, Closed) | Open |

### JobApplication
| Field Name | Data Type | Description | Constraints | Example |
| :--- | :--- | :--- | :--- | :--- |
| **ApplicationID** | Integer | Unique application ID | Primary Key, Not Null | 9001 |
| **JobSeekerID** | Integer | Unique identifier for job seeker | Foreign Key from JobSeekerProfile, Not Null | 123456 |
| **JobID** | Integer | Unique job identifier | Foreign Key from JobPosting, Not Null | 1023 |
| **ApplicationDate** | DateTime | Date the job seeker applied for the job | Not Null | 2026-01-15 12:31 |
| **ApplicationStatus** | Enum | Application status of the job seeker for a specific job | Not Null; (Shortlisted, Accepted, Rejected) | Shortlisted |

### Chat History
| Field Name | Data Type | Description | Constraints | Example |
| :--- | :--- | :--- | :--- | :--- |
| **MessageID** | Integer | Unique message ID | Primary Key, Not Null | 880001 |
| **SenderUserID** | Integer | Unique identifier for the person who sent the specific message | Foreign Key from JobSeekerProfile/ RecruiterProfile, Not Null | 123456 |
| **MessageText** | Text | Message content | Not Null | …can I know more about this job… |
| **SentAt** | DateTime | Date and time the message is sent | Not Null | 2026-01-15 12:31 |