 🖧 🔒 Network Vulnerability Assessment and Hardening

### We have conducted a security assessment and penetration testing using Gray-box Methodology against both internal and external assets of the Holo Cooperate Network.
 ![image](https://github.com/user-attachments/assets/62a80215-0dbc-4574-bbf0-129b1f460e69)

### Simulating a real-world attacker with limited insider knowledge, we successfully uncovered and exploited multiple vulnerabilities—some of which resulted in privilege escalation, unauthorized access to critical systems, and full network compromise.These findings highlight serious risks and emphasize the need for promptremediation to enhance the organization’s overall security posture.
---

## 🎯 Objectives
- Conduct comprehensive pentesting process to detect security weaknesses.
- Implement hardening measures to strengthen system defenses.
- Provide actionable insights to improve overall security posture.

---
## Scope
|    Network                   | IP Range            |
|------------------------------|----------------------|
| External (Public-facing Network) | 10.200.110.0/24  |
| Internal Network             | 192.168.100.0/24     |


## 👥 Team Members  

| 🏅 Name            | 🎭 Role   |
|------------------|-----------|
|  Khaled Ahmed   | 🔹 Team Leader  |
| Mohammed Saeed   | 🔹 Member  |
| Ahmed Essawy   | 🔹 Member  |
| Youssef Mohammed | 🔹 Member  |
| Hazem Alaa      | 🔹 Member  |

--- 

## 📌 Project Breakdown  


- Reconassance including full port scanning, Vhost scaning and directories scan
  
   ![image](https://github.com/user-attachments/assets/4df80cb8-09cb-4f5d-8ec1-a7720272bf34)
   ![image](https://github.com/user-attachments/assets/c7d7749e-fcfa-4044-99cb-734f0d1f6806)

- Vulnerabilities exploitation and stimulating to unauthorized access (we have prior permission from the holo coperate to do this)
   * Example: RCE vulnerability gave us a Full reverse shell over host ip:10.200.110.33 | container IP: 192.168.100.100
     ![image](https://github.com/user-attachments/assets/8072c162-53b4-4c60-9a61-6f000e71dade)
     ![image](https://github.com/user-attachments/assets/2847851c-016d-47bb-857e-2b812a3caf68)
     ![image](https://github.com/user-attachments/assets/8aa45d92-b736-4ae0-830e-e100c068985c)

   
- Enumeration on all the accessed machines
  * Examples:
      * Gained accessing to the internal network 192.168.100.0/24
    
        ![image](https://github.com/user-attachments/assets/85b6ca20-da85-4aa4-ae9f-020fbea8cc3d)
    
      * After enumerating the container with ip 192.168.100.100 we found a database credentials in  `db_connect.php` file
    
          ![image](https://github.com/user-attachments/assets/0ec7023b-1457-42ad-b433-d60547cac07b)


- previlage esclation and Lateral movement

  * Exmples:
      * After gaining access to the machine 192.168.100.100 we found using scanning that 192.168.100.1 is running sql server so we used the DB creds we found in the previous step to log in to the machine
      * and injected RCE payload in the mysql table and use outfile function with select statment to make a file contaning the RCE payload on the 192.168.100.1 maching then we used the rce to get a reverseshell and gain full access to the gateway
      * we now on the 192.168.100.1 machine but stil www.data user, then we found a docker binary with suid and we exploited it ot gain root acess
    
         ![image](https://github.com/user-attachments/assets/83f9164a-d501-4c12-9ae4-533eb8899f52)
         ![image](https://github.com/user-attachments/assets/18a62b44-cca0-4c7a-a1ca-ca640c5d9774)
         ![image](https://github.com/user-attachments/assets/aa481f7b-3160-465c-9512-903f87896b78)
         ![image](https://github.com/user-attachments/assets/9a476ee4-709c-4ca5-8631-62ce7cb3995e)
         ![image](https://github.com/user-attachments/assets/a719d556-b47a-4cf7-bbb2-f4bfc0f50ae0)
         ![image](https://github.com/user-attachments/assets/1e452964-e850-4787-b26d-eba6cf50d02b)

    
    
- Reporting stage

  * we have made a full comperhensive report about all the vulnerabilities and the remediation steps you can find it under the report section in the repo
  * or through the  following google drive link (Trust me not a malisious link 😁) : https://drive.google.com/file/d/1SutbhuGgngDXLznqXvZuL21u2K_SvjWB/view?usp=sharing
  * Thm Certifications that helped us with knoweledge to be able to do the testing is also mentined in the tryhackme certs section or through this link: https://drive.google.com/file/d/127_gMgM1UXNa1j8Dm8H8EHgmPM30hY56/view?usp=sharing
  
 --- 

### Final Note:

This project was the result of dedicated hard work and true teamwork. Throughout the process, we gained valuable insights into key cybersecurity concepts, including Active Directory, Kerberos authentication, lateral movement, containers, antivirus evasion, and more.
It was a rewarding experience that significantly deepened our understanding and skills.


---

## ⚠️ Disclaimer  
This project is for educational and ethical use only. Unauthorized testing on real systems is illegal. We do not endorse misuse and are not responsible for any unethical actions. Always adhere to legal and ethical guidelines.  

---

## 📬 Contact  
For inquiries, collaborations, or contributions, feel free to contact the **Team Leader**:  
**🔹 Khaled Ahmed**  
📧 [khaled.emam.official@gmail.com]  

Last Updated: may 10, 2025


