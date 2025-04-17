# Wazuh

## Objective

To gain hands-on experience in deploying and using Wazuh, an open-source security information and event management (SIEM) platform, for host-based intrusion detection, log analysis, and real-time threat monitoring in a simulated SOC environment.

## Skills Learned

- 🛠️ SIEM Deployment: Configured Wazuh Manager, Agent, and Dashboard components for centralized monitoring.
- 🚨 Alert Correlation: Investigated Wazuh-generated alerts, reviewed rulesets, and identified high-confidence security incidents.
- 🔒 Host-Based Detection: Monitored systems for unauthorized access attempts, privilege escalation, and malware indicators.
- 📊 Dashboard Navigation: Used the Kibana-based Wazuh dashboard to visualize and query event data for security insights.

## Exercises

Scenario:
![image](https://github.com/user-attachments/assets/a20c738d-303e-402a-95f8-645f76ab86f0)

Prepared the Wazuh environment to display data from Apr 29th, 2024 between 12:00 and 20:00
![image](https://github.com/user-attachments/assets/5120d4de-51c1-460f-bc0a-c441be5106dc)

511 events generated between 12:00 and 20:00
![image](https://github.com/user-attachments/assets/314f6ec4-ac86-4a51-b051-cbda66633f58)

In the search bar, searched for “localhost” and accessed the earliest timestamp to find the file downloaded for initial access.
![image](https://github.com/user-attachments/assets/c59854f3-4445-4e54-a547-5ec0bf16b7fb)
![image](https://github.com/user-attachments/assets/aab67a8e-8f3c-46c7-97cd-e66fce1b45de)

To find the suspicious command executed to create a schedule task, the word “scheduler” is searched for:
![image](https://github.com/user-attachments/assets/9abbb79f-a8b4-4f0d-a4dd-de95269d4b7e)

The command is set to run at 12:34.
![image](https://github.com/user-attachments/assets/30f4930a-ac30-4349-8525-f5e69e19e6ab)

In order to find what was encoded in the command above, the following string will be decoded:
![image](https://github.com/user-attachments/assets/e6087f85-37d7-4635-8b97-7383f8c014fb)

Using cyberchef, the string decodes to “ping www.youarevulnerable.thm”
![image](https://github.com/user-attachments/assets/924c5e56-4d6c-4e6a-adc9-755d3de398a3)

To find the password set for a new user account, first search the word “user” in the search bar:
![image](https://github.com/user-attachments/assets/d5d5f525-1725-4137-acb5-c3cecbeb849f)

The password “I_AM_M0NIT0RING” shows up while analyzing the logs:
![image](https://github.com/user-attachments/assets/7b3ae7ae-684a-445e-88c4-048e57f6fe72)

The software used to dump the credentials is called memotech.exe, which is used by the Mimikatz exploit:
![image](https://github.com/user-attachments/assets/51fdc9cf-10b7-48e8-85cf-108cda6e1d0e)



