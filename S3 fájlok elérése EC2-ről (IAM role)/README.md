# S3 fájlok elérése EC2-ről
## A cél az, hogy ne access key-t használjunk, hanem IAM role-t adjunk a gépnek. 

Első lépésként egy teljesen alap beállításokkal rendelkező Amazon Linux 2023 EC2-t indítottam. 

Neve a példa kedvéért: <mark>s3-ls</mark>

<img width="1273" height="751" alt="Képernyőfotó 2026-09-30 - 13 59 39" src="https://github.com/user-attachments/assets/bc27d50d-81b3-43ec-b7ec-17957fc33f03" />

Amint létrejött az EC2 akkor csatlakozunk hozzá

<img width="1144" height="267" alt="Képernyőfotó 2026-09-30 - 14 03 12" src="https://github.com/user-attachments/assets/60e8618a-97ef-4e71-a513-be2f5cc84f3f" />

Az alapbeállításokat meghagyjuk

<img width="1380" height="699" alt="Képernyőfotó 2026-09-30 - 14 03 32" src="https://github.com/user-attachments/assets/32e9f11a-8043-4f11-a80c-3f4b288edf4d" />

A CLI felületre belépve a következő kép fogad minket: 

<img width="1200" height="318" alt="Képernyőfotó 2026-09-30 - 14 03 48" src="https://github.com/user-attachments/assets/bf3b5d92-ae32-4ec2-b5d5-e562055916ec" />

A következő paranccsal: aws s3 ls s3://s3-alapok-4-599633425313-eu-north-1-an listázni kívánjuk a korábbi s3 bucketet amibe a statikus weboldalunkat helyeztük. 

Az eredmény: `Unable to locate credentials`

<img width="1199" height="336" alt="Képernyőfotó 2026-09-30 - 14 04 55" src="https://github.com/user-attachments/assets/a46c7088-40de-40a3-a812-d7da7a7b946e" />

Nincs jogosultságunk és elutasítja a rendszer a kérést. 

