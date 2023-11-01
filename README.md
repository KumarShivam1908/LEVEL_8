# LEVEL_8
This is the level 8 challenege of the event.

Given that you have the IP address 10.0.2.18, you can proceed to conduct an Nmap scan to gain insights into the target network.We'll use a comprehensive scan to check all available ports and enable version detection to identify the services running on those ports. Here's the command:

![image](https://github.com/KumarShivam1908/LEVEL_8/assets/119051305/8bcb8283-fd24-4a8f-ab03-11d683d37bc2)

Exploring FTP and SSH Services:

In the Nmap results for IP address 10.0.2.18, we observed that the FTP and SSH services are open and accessible. This presents an opportunity to investigate these services further.

We'll start by focusing on FTP (File Transfer Protocol) and explore the possibility of anonymous login. Anonymous FTP login is a common way to access publicly available files without the need for authentication.

![image](https://github.com/KumarShivam1908/LEVEL_8/assets/119051305/7737379b-9b71-47b2-b8ed-1891bbd581e7)

In the course of our exploration, we discovered an 'introduction.txt' file on the FTP server, which contains the username 'ZODICLOWN' in all capital letters. Now that we have the username and are aware that the SSH service is available, we can attempt to gain access to the system via SSH. However, access requires a password, and to uncover it, we will employ a password brute-force approach using a tool like 'Hydra' to systematically try various password combinations in an attempt to gain entry.

![image](https://github.com/KumarShivam1908/LEVEL_8/assets/119051305/a21f0a10-2cee-4a1d-bb01-42d9b5f13c3e)

Upon utilizing Hydra for a password brute-force attack, we successfully retrieved the password, which is 'cookie.' With the obtained credentials in hand, we can now proceed to access the system via SSH and embark on an exploration to uncover the content and resources it holds
Upon gaining access to the system, we found two folders named 'chitchat' and 'plans.' Both folders contained numerous files, but the key clue was discovered in the 'chitchat/personal_conv.txt' file. This file revealed an image link, which serves as an intriguing lead for our further investigation.

![image](https://github.com/KumarShivam1908/LEVEL_8/assets/119051305/6856edcd-a3a0-440a-897f-63f1c9bce78f)













