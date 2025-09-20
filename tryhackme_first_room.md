\# TryHackMe — offensive security intro

\*\*Date:\*\* 2025-09-20  

\*\*Platform:\*\* TryHackMe    

\*\*Difficulty:\*\* Easy 

\*\*Time Spent:\*\* <e.g.  15m>   

---



\## Summary / Objective

This is a walkthrough for the TryHackMe room \*\*Offensive Security Intro\*\*. The objective was to enumerate the target, identify Admin Page, and transfer money to my account. All testing was performed in the TryHackMe controlled environment and follows the platform rules.



---



\## Scope \& Rules

\- Platform: TryHackMe — lab environment provided by platform.  

\- Allowed: attacking the assigned machine(s) only, no external attacks.  

\- Not allowed: any testing outside the lab environment (not performed).



---



\## Target

\- IP: `not needed in attack`  

\- Notes: Vm is a beginner-friendly box focusing on web enumeration and basic privilege escalation.



---



\## Tools \& Methodology

Tools used :  `gobuster`

Methodology: follow a structured approach — reconnaissance → enumeration → exploitation (proof-of-concept) → post-exploitation → cleanup.



---



\## Enumeration



\### 1) Port scan

Command used: gobuster -u <url> -w wordlist.txt dir



