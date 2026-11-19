# SQL Injection: Research & Vulnerability Analysis

## Project Overview

This project explores **SQL Injection (SQLi)**, a web application vulnerability that allows attackers to manipulate database queries through improperly handled user input.

Originally developed as a collaborative capstone research project for **CodePath CYB101**, this work was expanded through two independently completed, hands-on labs using PortSwigger Web Security Academy.

The objective was to strengthen my understanding of how SQL injection vulnerabilities operate, examine their potential security impacts, and explore strategies for preventing them.


## 1. Research: Understanding SQL Injection

As part of our CodePath CYB101 capstone, my group researched SQL injection (SQLi), its underlying mechanisms, security implications, and mitigation strategies.

Our collaborative research covered:

- **SQLi Fundamentals:** How improperly handled user input can manipulate database queries.
- **Organizational Impact:** How SQLi can compromise sensitive information, disrupt systems, and lead to financial and reputational damage.
- **Real-World Case Studies:** Examining documented SQL injection vulnerabilities and their consequences.
- **Mitigation Strategies:** Exploring preventive measures such as parameterized queries, secure database practices, and web application firewalls (WAFs).

### My Research Contributions

My individual research focused on two key areas: **the effects of SQL injection on organizational security** and **a real-world case study involving the MOVEit Transfer vulnerability (CVE-2023-34362)**.

#### Effects of SQL Injection

I researched the potential consequences of SQL injection vulnerabilities, including:

- **Data Exposure:** Unauthorized access to sensitive information, including personally identifiable information (PII), financial records, and confidential organizational data.
- **Financial Losses:** Potential regulatory fines, recovery costs, legal expenses, and other financial consequences following a security incident.
- **Reputational Damage:** Loss of customer trust, diminished organizational credibility, and negative publicity.
- **System Compromise:** How SQL injection can enable additional malicious activity, including malware deployment, service disruption, and persistent unauthorized access.

These findings highlighted how SQL injection can have consequences beyond the initial vulnerability, affecting an organization's data security, operations, finances, and reputation.

#### Real-World Case Study: MOVEit Transfer (CVE-2023-34362)

As part of my individual research, I examined **CVE-2023-34362**, a critical SQL injection vulnerability affecting Progress MOVEit Transfer, a managed file transfer application.

Disclosed in 2023, this vulnerability could allow unauthenticated attackers to gain unauthorized access to the application's database.

The vulnerability was actively exploited by the CL0P ransomware group during a widespread attack campaign involving data theft and the deployment of malicious web shells.

This case study demonstrated how SQL injection can contribute to larger security incidents, reinforcing the importance of timely patching, vulnerability management, and secure application development.

**Case Study References:**

- [NIST National Vulnerability Database — CVE-2023-34362](https://nvd.nist.gov/vuln/detail/CVE-2023-34362)
- [CISA — CL0P Ransomware Gang Exploits MOVEit Vulnerability](https://content.govdelivery.com/accounts/USDHSCISA/bulletins/35ecb08)
- [Progress Software — MOVEit Transfer Security Advisory](https://community.progress.com/s/article/MOVEit-Transfer-Critical-Vulnerability-31May2023)

### Capstone Presentation

[View Our SQL Injection Capstone Presentation](research/CYB101_SQLi_Capstone.pdf)

*The presentation was developed collaboratively as part of CodePath CYB101. My individual research contributions focused on the effects of SQL injection and the MOVEit Transfer case study.*


## 2. Hands-On Vulnerability Analysis

Following the research component, I independently completed two guided SQL injection labs through **PortSwigger Web Security Academy**, using its intentionally vulnerable training environments.

The purpose was to observe how SQL injection can affect application behavior and connect the concepts explored during our research to practical examples.

| Lab | Objective | Outcome |
|---|---|---|
| **[01 — Hidden Data Retrieval](lab/01-hidden-data-retrieval/README.md)** | Manipulate a SQL `WHERE` clause to bypass product restrictions | Successfully retrieved products beyond the original category restrictions |
| **[02 — Authentication Bypass](lab/02-authentication-bypass/README.md)** | Manipulate a login query to bypass password verification | Successfully authenticated as the administrator without the correct password |

Both labs were successfully completed.

Each lab's documentation includes the testing process, SQL injection payload, observations, security impact, and screenshots.

## 3. Key Findings

The two exercises demonstrated different security consequences arising from the same underlying vulnerability.

**Hidden Data Retrieval**

Manipulating a product-category parameter with an always-true condition altered the intended query logic, allowing the application to expose products that should have remained restricted.

**Authentication Bypass**

Manipulating a username input allowed the password verification condition to be excluded from the effective query, resulting in unauthorized administrator access within the lab environment.

Both demonstrations reinforced the importance of treating user-controlled input as data rather than executable SQL instructions.

## 4. Mitigation Strategies

The following defensive practices can help prevent or reduce the impact of SQL injection vulnerabilities:

- **Parameterized Queries:** Separate SQL commands from user-supplied values to prevent manipulation of query structure.
- **Web Application Firewalls (WAFs):** Help identify and block suspicious requests as an additional layer of protection, rather than a substitute for secure query construction.
- **Input Validation:** Enforce appropriate input constraints as an additional defensive measure.

## 5. Reflection

One of my biggest takeaways from this project was seeing how seemingly small changes to user input could significantly alter the behavior of an application.

While our capstone research introduced me to SQL injection's mechanisms, impacts, and mitigation strategies, completing the hands-on labs helped reinforce those concepts through practical observation.

I particularly enjoyed understanding **why the injection payloads worked**, how they manipulated SQL query logic, and the security implications of their results.

This experience further strengthened my interest in cybersecurity, particularly in understanding how vulnerabilities are exploited and how technical analysis can contribute to stronger security practices.

## 6. Acknowledgments

The research component was completed collaboratively as part of **CodePath CYB101**.

Thank you to CodePath, instructor Jean Leconte, TF Jasmine Sutton, and my capstone teammates for their guidance, support, and collaboration.

**Capstone Team:** Jasmine Sharpe, Alice Jiang, Jennifer Isaac, Muhammadkhon Yakubov

The PortSwigger labs and accompanying documentation were completed independently.



## 7. References & Additional Resources

### SQL Injection Fundamentals
- [W3Schools — SQL Injection](https://www.w3schools.com/sql/sql_injection.asp)
- [Microsoft Learn — SQL Injection](https://learn.microsoft.com/en-us/sql/relational-databases/security/sql-injection?view=sql-server-ver17)
- [PortSwigger Web Security Academy — SQL Injection](https://portswigger.net/web-security/sql-injection)
- [Invicti — SQL Injection (SQLi)](https://www.invicti.com/learn/sql-injection-sqli)
- [MITRE — CWE-89: Improper Neutralization of Special Elements Used in an SQL Command](https://cwe.mitre.org/data/definitions/89.html)

### SQL Injection Prevention & Mitigation
- [Cisco — What Is a Web Application Firewall (WAF)?](https://www.cisco.com/site/us/en/learn/topics/security/what-is-web-application-firewall-waf.html)
- [Codecademy — Preventing SQL Injection Attacks](https://www.codecademy.com/learn/seasp-defending-node-applications-from-sql-injection-xss-csrf-attacks/modules/seasp-preventing-sql-injection-attacks/cheatsheet)
- [W3Schools — SQL Prepared Statements](https://www.w3schools.com/sql/sql_prepared_statements.asp)

### Real-World Case Study
- [NIST National Vulnerability Database — CVE-2023-34362: MOVEit Transfer SQL Injection](https://nvd.nist.gov/vuln/detail/CVE-2023-34362)
- [CISA — CL0P Ransomware Gang Exploits MOVEit Vulnerability](https://content.govdelivery.com/accounts/USDHSCISA/bulletins/35ecb08)
- [Progress Software — MOVEit Transfer Security Advisory](https://community.progress.com/s/article/MOVEit-Transfer-Critical-Vulnerability-31May2023)

### Video Resources
- [SQL Injection — YouTube Video](https://www.youtube.com/watch?v=vqnfc4bJigo)
- [SigPWNY (University of Illinois Urbana-Champaign) — SQL Injection](https://www.youtube.com/watch?v=nOKu8UnN29k)

### Independent Hands-On Labs
The following PortSwigger Web Security Academy exercises were completed independently to reinforce concepts covered in the CodePath CYB101 capstone research.

- [SQL Injection: Retrieving Hidden Data](https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data)
- [SQL Injection: Login Bypass](https://portswigger.net/web-security/sql-injection/lab-login-bypass)


---

**Disclaimer:** All hands-on testing was conducted within PortSwigger Web Security Academy's authorized, intentionally vulnerable training environments for educational purposes.
