# Password Security

## Task 1 --- Test a Weak Password

Run:

    echo "password123" | cracklib-check

### Screenshot

<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/3c986d09-00b5-4378-a668-e257d498d6e2" />


### Questions

1.  What does the tool say about the password?
   - The tool said about the password, password123 is based on dictionary word.
2.  Why is this password weak?
   -This password is weak because it relies on a common dictionary word (password) rather than a random or unpredictable passphrase.Andalso, appending simple sequential numbers (123) is a predictable pattern that attackers and password-cracking tools automatically test.Moreover, it lacks complexity and sufficient unpredictability against automated guessing.

### Reflection

Explain why weak passwords are dangerous.
- This passwoed is weak because fast cracking via dictionary and brute-force attacks.Unauthorized account and system access: Once compromised, an attacker can read sensitive data, alter settings, or pivot to        other systems.Futhermore, Credential stuffing risk: If the same weak password is reused across multiple accounts or services, a breach on one site can expose accounts elsewhere.

------------------------------------------------------------------------

## Task 2 --- Test a Strong Password

Run:

    echo "Tr4!nBicyclePlanet" | cracklib-check

### Screenshot

<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/df276de0-8607-40e7-b176-784ab453a882" />


### Questions

1.  What result did the tool return?
    - When passed cleanly (using single quotes: echo 'Tr4!nBicyclePlanet' | cracklib-check), cracklib-check should return Tr4!nBicyclePlanet: OK (meaning it passes standard dictionary), whereas using double             quotes in bash triggers bash: !nBicyclePlanet: event not found before cracklib-check runs.
    
2.  What characteristics make this password stronger?
   - The characheristics make it stronger password are:
     - Length
     - Complexity
     - Multi-word structure

### Reflection

Describe at least three characteristics of strong passwords.
- Three characheristics of strong password are :
  - Length: At least 12–16+ characters (the longer, the harder to crack).
  - Complexity: A mix of uppercase, lowercase, numbers, and special symbols.
  - Unpredictability: Avoids common words, personal info, and simple patterns like 123.

------------------------------------------------------------------------

## Task 3 --- Password Analysis

Evaluate the following passwords:

-   123456
-   qwerty
-   P@ssword1
-   correcthorsebatterystaple

### Questions

1.  Which passwords are weak?
   - 123456
2.  Which password is strongest?
    -correcthorsebatterystaple
3.  Why?
    - Due to it length and multi-word passphrase.

### Reflection

Explain what you learned about password strength.
- Length and unpredictability matter far more than short, complex-looking character substitutions. Attackers easily guess common patterns, keyboard walks, and dictionary words disguised with symbols (like P@ssword1), whereas a long passphrase made of multiple unrelated words provides much stronger protection against both dictionary and brute-force attacks.
