# Yagi_Typhoon_Donation_Tracker
Extracting transactions from 200k+ rows PDF file &amp; PowerBI Dashboard

Hello everyone,

Yagi swept through Northern Vietnam and brought a massive destruction on people’s lives, families & houses, leading to $US 2.0B loss. There's a risk of embezzlement or fraud involving donations from certain organizations and individuals, which is truly condemnable! I've created this PowerBI Dashboard, both to serve as a learning tool and to help people investigate any suspicious transactions.

Repo structure:
1. Ingestion Donation records from 6 PDF files with 200K+ row each
2. Data Processing to fit for PowerBI Dashboard data loading
3. PowerBI Dashboard link: https://mavenanalytics.io/project/19637

Key Features:
- Set Thresholds for what amount qualifies as a Red Flag for organizations and companies. For example, I currently have it set to flag transactions below 500k for organizations or companies, which has highlighted a total of 5,873 transactions that need attention.
- Search for specific information or filter out suspicious transactions. Similarly, on page 2, I've provided a detailed table that allows users to search through various fields, including names, groups, and gender (which may not be entirely accurate due to data processing).
- Top Contributors and a small section called "Warm Heart Messages" featuring heartfelt messages from young children contributing in their own small ways. ❤️
  
Some observations:
- As of September 12th, the total recorded amount was about 220 billion VND, with 309k contributions. The most common amount is 200k (median value). The majority, 50%, of transactions fall into the 100-500k range. The group with amounts under 50k (which might include suspicious transactions) makes up only about 6%, so it seems like just a few bad apples.
- Daily contributions were slow at the beginning of the month but spiked 10x on September 9th and 15x on September 10th. This might be due to news about the landslides in "Làng Nủ" catching people's attention. Contributions then dropped significantly, possibly due to incomplete data from VCB's statements.
- With a threshold set for Red Flag transactions below 500k, there are about 5,873 suspicious transactions, many from individuals considered famous or from organizations. Some transactions were as low as just a few thousand, 10k, or under 50k. You can explore further to investigate.
- Top Contributors: Besides singers and actors like Hòa Minzy and Sofia, who contributed around 400 million VND, a group of OKVIP members also made significant contributions, totaling about 8 billion VND. (You can Google what OKVIP is 😉).

Data processing and analysis method:
- Main Source: The "Vietnam Fatherland Front," which includes all transactions from VCB, Vietinbank, Agribank, and BIDV. More updates will follow.
- Data extraction from PDFs to CSV files: I used Python to parse PDFs for VCB, while for other banks, I used CSV files exported by the J2TEAM to save time. Many thanks to J2TEAM for their support!
- Filtering Vietnamese Names: I tried using several NLP libraries to detect Vietnamese names from transaction notes, such as SpaCy, a popular NLP library, with adjustments for Vietnamese names. Based on this, I classified them by gender (male/female). However, the NLP processing was too slow, so I created some rules to speed up the filtering, which may reduce accuracy.
- I defined Red Flag transactions as those involving certain groups, companies, or unexpectedly low amounts from influential people. You can adjust the threshold for Red Flags as you see fit. This is to help with further investigation, but I am not making any claims about whether there is fraud or not.
- Since there could be errors in the data processing, I take no responsibility for any issues or complaints regarding this dashboard.

Wishing the people of Vietnam good health and hoping for a speedy recovery from the aftermath of Typhoon Yagi.
---------
PowerBI Dashboard link: https://mavenanalytics.io/project/19637


![1](https://github.com/user-attachments/assets/9edea701-4e0d-4e53-b6ed-f8a6390c5197)
![2](https://github.com/user-attachments/assets/b5907bdf-d5d2-481b-ae4b-a13cadf476dd)
![3](https://github.com/user-attachments/assets/ea64fa0f-c182-4780-8945-21bacdb7e9e8)
![4](https://github.com/user-attachments/assets/40b973cc-640c-48d1-b5c0-7a889df31991)

