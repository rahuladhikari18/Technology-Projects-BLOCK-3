# Phishing Investigation

## Task 1 --- Analyse a Suspicious Email

>**Subject**: ⚠ Urgent: Your Account Will Be Locked in 24 Hours!
>
>**From**: Security Team <support@secure-verification-update.com>
>
>**To**: you@example.com
>
>Hello User,
>
>We detected unusual activity on your account. For your security, your access will be temporarily suspended within 24 hours unless you verify your information.
>
>Please click the link below to avoid interruption:
>
>👉 Verify Your Account Now
[http://secure-update-verification.com/login-confirmation](https://secure-update.verify-account-check.example.com/login/redirect/authentication_step2/?sessionid=3f9a2b8c7d1e44aa92f1b0f8f&token=invalid123456789&continue=http%3A%2F%2Fupdate-alert-confirmation.example.net%2Fverify%2Fuser%2Fsecurity%2Fcheck%2F?id=889201&source=email_warning)
>
>Failure to verify may result in permanent loss of access and data.
If you believe this is a mistake, reply with your full name, date of birth, and password so we can assist you.
>
>**Thank you,**
>
>**Account Support Team**
>
>**Security Department**



### Questions

1.  Who appears to be the sender?
   - Security Team <support@secure-verification-update.com> appear to be the sender.
     
2.  Does the email create urgency or pressure?
   - Yes, the email create urgency or pressure.
     
3.  Are there spelling or grammar mistakes?
   - No, there is not spelling or grammar mistakes.
     
4.  Does the link match the organisation domain?
   - No, the link dorsnot match the organization domain.

### Reflection

Explain why attackers use phishing emails.
- Attackers use phishing emails because exploiting human psychology is often much easier, cheaper, and faster than breaking through technical security defenses like firewalls or encryption.
   Here are the main reasons why phishing is such a common attack method:
    - To bypass technical defenses by exploiting human trust rather than hacking systems directly.
    - To steal sensitive data like passwords, login credentials, and financial details.
    - To deliver malware (such as ransomware or spyware) via malicious links or attachments.
    - To scale attacks cheaply, reaching millions of targets at almost no cost.
    - To manipulate emotions (fear, urgency, or curiosity) so victims act without thinking.  
    - To gain internal access to a company's network through a single compromised employee.   

------------------------------------------------------------------------

## Task 2 --- Link Inspection

Hover over the link in the email (or copy link) and inspect the URL.

### Screenshot

 <img width="1920" height="1200" alt="Screenshot (3)" src="https://github.com/user-attachments/assets/89f90737-5167-4998-8cbe-109cc7f75817" />


### Questions

1.  Does the displayed link match the actual URL?
   - No, the displayed link doesnot match the actual URL.
     
2.  Are there unusual domain names?
   - Yes, there are unsual domain names.

### Reflection

Explain why users should always inspect links before clicking them.
- Attackers frequently disguise malicious destinations using deceptive display text, lookalike domains, or redirect chains so a link appears trustworthy at a glance. Inspecting a link by hovering over it or copying it first helps you spot mismatches between the visible text and the real destination before your browser ever makes a request—protecting you from credential harvesting, malware downloads, session hijacking, and account takeovers.
