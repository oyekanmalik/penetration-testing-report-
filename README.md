Week 4 – Mediroza General Hospital Penetration Testing Report

Author: Oyekan Malik Atanda
Program: NetworkWalks Cybersecurity Internship
Batch: B084
Week: 4
Assessment Type: Web Application Penetration Testing
Target: Mediroza General Hospital
Environment: Kali Linux

⸻

Project Overview

This project involved conducting a web application penetration-testing assessment against Mediroza General Hospital as part of my Week 4 cybersecurity internship activities.

The assessment focused on identifying security weaknesses in the hospital’s web application, evaluating authentication mechanisms, examining document security, identifying information disclosure issues, and assessing the risks associated with exposed files and database backups.

The exercise helped demonstrate how multiple vulnerabilities can be chained together to create a significant security risk to an organization.

Objectives

* Identify vulnerabilities within the web application.
* Evaluate authentication and access-control mechanisms.
* Investigate SQL injection vulnerabilities.
* Assess the security of password-protected PDF documents.
* Examine PDF metadata for sensitive information disclosure.
* Identify exposed directories and backup files.
* Understand the potential impact of data exposure.
* Provide security recommendations to mitigate identified risks.

Scope of Assessment

The assessment focused on the following areas:

* Public-facing hospital web application.
* Patient portal and login functionality.
* Laboratory report access and document security.
* PDF password protection.
* Metadata analysis.
* Exposed directories and database backup files.
* Database error messages and information disclosure.

Tools Used

Tool	Purpose
Kali Linux	Penetration-testing environment
Web Browser	Web application discovery and manual testing
John the Ripper	Password recovery testing
ExifTool	PDF metadata inspection
pdf2john	PDF hash extraction for password testing
NetworkWalks Password Cracker	Controlled password-recovery testing
HTTP/Web Requests	Validation of accessible web resources

Key Findings

The assessment identified several security weaknesses that could potentially compromise sensitive information.

1. SQL Injection and Authentication Bypass

A vulnerability in the patient login functionality allowed authentication controls to be bypassed through manipulated input, potentially permitting unauthorized access to the patient portal.

Risk Level: Critical

2. Unauthorized Access to Patient Laboratory Reports

Multiple laboratory reports were accessible after authentication controls were bypassed, demonstrating weaknesses in access control and protection of confidential medical information.

Risk Level: Critical
[Mediroza_Report_Week4_B084_Purple_Final.pdf](https://github.com/user-attachments/files/35333944/Mediroza_Report_Week4_B084_Purple_Final.pdf)

3. Weak PDF Password Protection

Password-protected laboratory reports were secured with weak passwords that could be recovered through dictionary-based password testing.

Risk Level: High

4. Sensitive PDF Metadata Exposure

Metadata inspection revealed internal information that provided clues about the location of a database backup directory.

Risk Level: High

5. Publicly Accessible Database Backup

A database backup was discovered in a publicly accessible directory. The backup contained sensitive staff and shareholder information, creating a serious confidentiality and privacy risk.

Risk Level: Critical

6. Verbose Database Error Disclosure

The application exposed database error messages during testing. Such errors may reveal technical information that could assist an attacker in identifying and exploiting application weaknesses.

Risk Level: Medium

Risk Summary

Vulnerability	Risk Level
SQL injection authentication bypass	Critical
Unauthorized access to patient reports	Critical
Weak PDF passwords	High
Sensitive PDF metadata exposure	High
Publicly accessible database backup	Critical
Database error disclosure	Medium

Recommendations

Based on the findings, the following security improvements are recommended:

* Implement prepared statements and parameterized SQL queries.
* Strengthen authentication and session-management controls.
* Enforce proper authorization for patient records and report downloads.
* Remove database backups from publicly accessible directories.
* Disable directory listing on web servers.
* Use strong, unique passwords and improved document-access controls.
* Remove sensitive metadata from documents before publication.
* Disable verbose database error messages in production.
* Monitor authentication activity and unusual file-access requests.
* Conduct follow-up security testing after remediation.

Learning Outcomes

Through this assessment, I gained practical experience in:

* Web application reconnaissance and security testing.
* Identifying SQL injection vulnerabilities.
* Understanding authentication bypass risks.
* Evaluating document password security.
* Inspecting file metadata using Exfoliate.
* Identifying publicly exposed directories and backup files.
* Understanding confidentiality and data-exposure risks.
* Writing security findings and remediation recommendations.

Conclusion

This assessment demonstrated how weaknesses in authentication, access control, document protection, metadata management, and backup security can combine to expose sensitive organizational information.

It reinforced the importance of layered security, secure coding practices, proper data handling, and continuous security assessment.

This project represents part of my ongoing cybersecurity learning journey and practical experience during my NetworkWalks internship.

⸻

Disclaimer

This project was conducted as part of a cybersecurity learning and authorized laboratory assessment. The information is documented for educational and defensive-security purposes. Penetration-testing activities should only be performed on systems for which proper authorization has been obtained.
