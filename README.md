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

After successfully logging in via SSH, we decided to check the list of users present on the system, which can be found in the '/etc/passwd' file. In doing so, we discovered the existence of two user accounts, 'zodiclown' and 'zodiac.' This observation led us to the inference that the 'zodiac' user account may hold significant information, motivating us to explore its home directory and potentially gain root-level access.
![image](https://github.com/KumarShivam1908/LEVEL_8/assets/119051305/76410b2b-25b0-46dd-9b4f-10100b3c5f8e)



We again go back to zodiclown's home folder, we found two folders named 'chitchat' and 'plans.' Both folders contained numerous files, but the key clue was discovered in the 'chitchat/personal_conv.txt' file. This file revealed an image link, which serves as an intriguing lead for our further investigation.

![image](https://github.com/KumarShivam1908/LEVEL_8/assets/119051305/6856edcd-a3a0-440a-897f-63f1c9bce78f)

Following the provided image link, we encountered an image featuring 'Gothic Z.' We proceeded to download this image and initiated our steganographic skills for analysis. This technique involves examining the image for hidden information or messages concealed within it.
Utilizing initial tools like 'exiftool' and 'strings,' we uncovered a passphrase, which turned out to be 'topsecret.' This discovery strongly suggested the presence of hidden information within the image. With this in mind, we applied 'steghide' to extract concealed data, revealing a file containing a Drive link associated with Zodiac's activities.

![image](https://github.com/KumarShivam1908/LEVEL_8/assets/119051305/eb4d0295-72c5-4496-a80f-c8df1a381e56)

Upon accessing the Drive link, we encountered a hexhue. To decode this information, we utilized the online tool found at https://www.dcode.fr/hexahue-cipher.

![image](https://github.com/KumarShivam1908/LEVEL_8/assets/119051305/8af5160e-be15-4a35-91e4-fa61a0538f15)

After deciphering, the result revealed the password 'ERD3NC0RP,' which granted us access as the root user, further advancing our investigation.

After obtaining the root password and successfully logging in, we navigated to the 'zodiac' user's home directory. Inside this directory, we encountered a 'Final_Flag' folder. Within the 'Final_Flag' folder were six text files. The final text file, upon inspection, revealed the ultimate flag: 'zyp{Congrats_ERD3NC0RP}'—marking the successful conclusion of our exploration and the attainment of the flag.

![image](https://github.com/KumarShivam1908/LEVEL_8/assets/119051305/6ada329a-d738-44de-81f6-29db09be6caa)


Hope, you liked the challenge,do give me your feedback about this challenge.
By-Kumar Shivam
Linkedin:https://www.linkedin.com/in/kumar-shivam-b8b196258/



















