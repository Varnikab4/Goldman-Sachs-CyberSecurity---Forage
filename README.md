# Goldman-Sachs-CyberSecurity---Forage

I just completed Goldman Sachs's Software Engineering on Forage. In the simulation I:
Completed a job simulation as a Goldman Sachs governance analyst responsible for assessing IT security and suggesting improvements.
Identified that the company was using an outdated password hashing algorithm by cracking passwords using Hashcat.

Analysis and Finding on the given passwd_dump.txt file 

I have cracked some of the given passwords with the help of hashcat and john hash 
mechanism : 
123456: e10adc3949ba59abbe56e057f20f883e  
123456789: 25f9e794323b453885f5181f1b624d0b  
qwerty: d8578edf8458ce06fbc5bb76a58c5ca4  
password: 5f4dcc3b5aa765d61d8327deb882cf99  
111111: 96e79218965eb72c92a549dd5a330112  
12345678: 25d55ad283aa400af464c76d713c07ad  
abc123: e99a18c428cb38d5f260853678922e03 
1234567: fcea920f7412b5da7be0cf42b8c93759  
password1: 7c6a180b36896a0a8c02787eeafb0e4c 
password!: 6c569aabbf7775ef8fc570e228c16b98 

Q1] Password Analysis: 
• Hashing Algorithm: The hashed passwords in the passwd_dump.txt file appear to 
use the MD5 algorithm, as identified by hashcat and hash-identifier on Kali Linux. 
• Encryption Mechanism: For encrypting plaintext, DES(Unix) has been used, which is 
a symmetric-key algorithm historically associated with Unix systems. 

Q2] Password Cracking Mechanisms: 
• Hashcat: Hashcat, a powerful password recovery tool, was utilized to crack the given 
password hashes. It determined that MD5 was the likely hashing algorithm. 
• John the Ripper: Another widely-used password cracking tool, John the Ripper, was 
also employed to crack the password hashes. It supports various hash algorithms and 
formats. 
Q3] Level of Protection: 
• The use of MD5 for hashing and DES(Unix) for encryption indicates weak protection 
for passwords. 
• MD5 is vulnerable to collision attacks, and DES(Unix) is considered outdated, posing 
security risks. 

Q4] Controls for Hardening Security: 
• Use Stronger Hashing Algorithms: Replace MD5 with more secure algorithms like 
SHA-256 or SHA-3 to resist attacks. 
• Key Strengthening: Implement salting and key stretching to slow down brute-force 
attacks. 
• Enforce Complex Passwords: Establish a policy requiring a mix of uppercase, 
lowercase, numbers, and special characters. 
• Regular Password Updates: Encourage or enforce regular password updates to 
minimize the impact of leaked passwords.

Q5] Insights into Password Policy: 
• Low Complexity: Common passwords like "123456," "qwerty," and "password" 
suggest a lack of complexity requirements. 
• Length Limitations: Short passwords like "abc123" and "qwerty" indicate a potential 
insufficient minimum password length policy. 

Q6] Password Cracking Tools: 
• Hashcat Analysis: Hashcat is proficient in cracking hashes and determining the 
hashing algorithm. It is essential for assessing password security and testing the 
resilience of the system against attacks. 
• John the Ripper Analysis: John the Ripper, like Hashcat, is a versatile tool for 
password cracking. It supports various hash algorithms and formats, providing 
additional options for penetration testing. 

Q7] Recommended Changes to Password Policy: 
• Increase Minimum Length: Set a minimum password length requirement to 
encourage the use of longer and more secure passwords. 
• Enforce Complexity: Implement a policy requiring passwords to include a mix of 
uppercase, lowercase, numbers, and special characters. 
• Regular Training: Educate users on password best practices, such as avoiding easily 
guessable passwords. 

Conclusion: The current password policy exposes the organization to significant security 
risks due to weak hashing algorithms and lack of complexity requirements. Implementing 
the recommended changes will strengthen the password security posture, making it more 
resilient against unauthorized access attempts. Regular use of robust password cracking 
tools like Hashcat and John the Ripper is crucial for organizations to proactively identify and 
address vulnerabilities in their security infrastructure. 

Note: It is essential to conduct a thorough review of the organization's security policies and 
practices to ensure comprehensive protection against potential threats. Regular security 
audits, employee training, and the adoption of up-to-date encryption and hashing standards 
are critical components of a robust cybersecurity strategy.
