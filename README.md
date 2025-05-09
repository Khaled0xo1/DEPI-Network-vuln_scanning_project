# 🖧 🔒 Network Vulnerability Assessment and Hardening

### We have conducted  a security assessment and penetration testing against using Gray-box technique on both internal and external assets of the Holo Cooperative Network.
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


- Reconassance including full port scanning, Vhost scaning and directories
  
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
- Reporting stage
  
     




---

## ⚠️ Disclaimer  
This project is for educational and ethical use only. Unauthorized testing on real systems is illegal. We do not endorse misuse and are not responsible for any unethical actions. Always adhere to legal and ethical guidelines.  

---

## 📬 Contact  
For inquiries, collaborations, or contributions, feel free to contact the **Team Leader**:  
**🔹 Khaled Ahmed**  
📧 [khaled.emam.official@gmail.com]  

Last Updated: February 20, 2025


