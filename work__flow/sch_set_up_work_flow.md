# 🛠️ SCHOOL SETUP WORKFLOW 
#### ( INITIAL SYSTEM SETUP)

**Steps:**
- School Admin registers school account:
```
relationship:admin vs school:

        One Admin ──────── One School
                (M : 1)

    

```

*“School Admin registers school account”*
👉 Meaning (Human Action)

This is what the admin does.

*It means:*
A real person (school admin) is signing up into your system

They are providing initial details
📝 Typical input data:
- Admin name
- Email
- Password
- School name
- Phone number

<!-- 
        1. create user with different roles :
         
         users:
           admin
           parent
           teacher
        
        2. admin creates school account(school modules) 

 -->
---





- System creates school profile
    
    ```
        CREATE TABLE school (
    school_id UUID PRIMARY KEY DEFAULT gen_random_uuid(),

    -- Identity
    name VARCHAR(150) NOT NULL,
    slogan VARCHAR(200),
    logo_url TEXT,

    -- Contact info
    email VARCHAR(150) UNIQUE NOT NULL,
    phone VARCHAR(30),
    address TEXT,
    state VARCHAR(100),
    country VARCHAR(100) DEFAULT 'Nigeria',

    -- Academic setup
    current_session VARCHAR(20), -- e.g. 2025/2026

    -- System metadata
    is_active BOOLEAN DEFAULT TRUE,
    subscription_plan VARCHAR(50) DEFAULT 'free',

    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP);
    
    ```


- Admin sets:
    - School name
    - Classes (JSS1, JSS2, Primary 1–6, etc.)
    - Subjects
    - Academic session (e.g. 2025/2026)

***insert into the tables for school profile***


---
- System initializes database structure for school
    *create the entire database tables*
---
**Output :**
* School is ready for operations
* Classes and subjects exist
* Academic session is active