# Exploring Your System's Security

## Task 1 --- List System Users

Run:

    cat /etc/passwd

### Screenshot
<img width="1600" height="1200" alt="WhatsApp Image 2026-11-22 at 6 46 57 PM" src="https://github.com/user-attachments/assets/0f86cd6c-50fd-4e3e-91a4-3e9918dfe6dd" />


### Questions

1.  How many users exist on the system?
 - There are 38 user accounts listed in the /etc/passwd file, including system accounts and normal users.
2.  Which accounts appear to be system accounts?
 - Accounts appearto be system accounts include:
    -root
    -daemon
    -www-data
    -nobody
    -sshd
    -messagebus
    -dnsmasq
    -avahi
   -systemd-network
       The team4 account appears to be a normal user account.
   
3.  Why do operating systems create system accounts?
   - To run background services and processes.
   -To improve security by giving services separate permissions.
   -To prevent services from accessing files they do not need.  

### Reflection

Explain why understanding system users is important for cybersecurity.
- Understanding system users is important because it helps manage permissions, protect files and improve system security. It also helps identify normal users and system accounts and prevent unauthorised access.

------------------------------------------------------------------------

## Task 2 --- Inspect Running Processes

Run:

    ps aux

### Screenshot

<img width="1600" height="1200" alt="WhatsApp Image 2026-11-22 at 6 54 12 PM" src="https://github.com/user-attachments/assets/909e7b4f-cc49-49d6-a2c7-2981d93200de" />


### Questions

1.  Which processes are running as `root`?
   -On Linux, root is the main admin account. The root processes shown are:
      -Bullet Startup & core system
      -Bullet Background kernel helper
      -Bullet System background
2.  Why can processes running as root be dangerous?
   - root has full, unrestricted control over the computer. A process running as root isn't stopped by normal permission rules—it can read or change system files, install software, and control other programs. If a root process has a bug or gets hacked, the attacker gets wide-open access to the whole system instead of being blocked.
     
3.  What could happen if a malicious program ran with root privileges?
    - If bad software or an attacker ran as root on Raspberry Pi , they could:
       -Bullet Take over the device
       -Bullet Steal private information
       -Bullet Stick around after a reboot
       -Bullet Break or attack things

### Reflection

What did you learn about system processes and security?
- A Linux system runs lots of behind-the-scenes kernel helpers and services alongside normal user apps. Keeping everyday apps under a normal user account—and only using root when truly needed—limits damage if something goes wrong or gets hacked.

------------------------------------------------------------------------

## Task 3 --- Identify Open Network Ports

Run:

    ss -tuln

### Screenshot

<img width="1280" height="960" alt="WhatsApp Image 2026-11-22 at 7 11 43 PM" src="https://github.com/user-attachments/assets/71d00c6a-3daf-4db4-abd0-fac9515530ac" />


### Questions

1.  Which ports are open?
  - lists of ports which are opened are :
    - UDP ports: 5353, 111, 49030, 47084
    - Bullet TCP ports: 111, 22, 631, 5201
      
2.  Which services appear to be listening?
   - The lists of services which are appeared to be listening are :
   - Port 22 (TCP)
   - Bullet Port 111 (TCP & UDP)
   - Bullet Port 631 (TCP, localhost only)
   - Bullet Port 5353 (UDP)
   - Bullet Port 5201 (TCP)
   - Bullet Ports 47084 & 49030 (UDP)
     
3.  Why might open ports represent a security risk?
   - An open port acts like an entry point that can receive network traffic from other devices (especially when bound to 0.0.0.0, *, or [::]).
      Bullet If a listening service has a bug, weak settings, or isn't meant to be exposed, an attacker could exploit it to probe, disrupt, or access your system

### Reflection

Explain the relationship between open ports and potential attack
surfaces.
- The relationship between open ports and potential attack surfaces are listed below :
   - Our attack surface is all the ways an attacker could try to reach or attack your system.
   - Bullet Each open port adds a network entry point to that attack surface, so fewer open ports and tighter bindings mean less exposure and lower risk.
