# Understanding File Permissions

## Task 1 --- Create a File

Run:

    touch secret.txt
    ls -l secret.txt

### Screenshot

<img width="1600" height="1200" alt="WhatsApp Image 2026-11-22 at 7 34 42 PM" src="https://github.com/user-attachments/assets/be8df672-c840-45d7-bcd8-14882ca32223" />


### Questions

1.  Who owns the file?
   - The owner of the files are:
     - User owner: team4
     - Bullet Group owner: team4
       
2.  What are the default permissions?
   - The permissions automatically assigned to a user, application, or service when access is first granted, unless an administrator or user changes them.
      - secret.txt shows -rw---x--x (611 in octal: rw- = 6 for owner, --x = 1 for group, --x = 1 for others).  
        Bullet Standard default permissions on Linux are typically -rw-rw-r-- (664) or -rw-r--r-- (644) depending on umask, so secret.txt already shows non-standard/modified permissions rather than a typical              default.

### Reflection

Why is file ownership important in Linux systems?
- File ownership is important in Linux because it determines who owns a file or directory and who is allowed to access, modify, or execute it. It is a fundamental part of Linux security and access control.
------------------------------------------------------------------------

## Task 2 --- Restrict File Permissions

Run:

    chmod 600 secret.txt
    ls -l secret.txt

### Screenshot
<img width="1280" height="960" alt="WhatsApp Image 2026-11-22 at 7 46 21 PM" src="https://github.com/user-attachments/assets/aacfa6bd-c116-4768-8b65-5c13421c23ce" />


### Questions

1.  Who can read the file now?
 - Everyone can read the file.
    - owner
    - group
    - other
      
3.  Who cannot access it?
   - Everyone can acess it because no user is blocked from accessing by the file own permission bits.


------------------------------------------------------------------------

## Task 3 --- Open Permissions (Security Risk)

Run:

    chmod 777 secret.txt
    ls -l secret.txt

### Screenshot

<img width="1280" height="960" alt="WhatsApp Image 2026-11-22 at 7 46 21 PM" src="https://github.com/user-attachments/assets/582e7892-f370-491f-aa5d-2e4ea60e4c7a" />


### Questions

1.  Who can access the file now?
   - Everyone can acess the file.
      - owner
      - group
      - other
      - 
3.  Why might this configuration be dangerous?
   - This configuration might be dangerous
      - Unauthorized data exposure
      - Tampering, corruption, or data loss
      - Arbitrary code execution / privilege escalation risk
      - Violation of least privilege

