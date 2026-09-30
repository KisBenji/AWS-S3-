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

A következő paranccsal: `aws s3 ls s3://s3-alapok-4-599633425313-eu-north-1-an` listázni kívánjuk a korábbi s3 bucketet amibe a statikus weboldalunkat helyeztük. 

Az eredmény: `Unable to locate credentials`

<img width="1199" height="336" alt="Képernyőfotó 2026-09-30 - 14 04 55" src="https://github.com/user-attachments/assets/a46c7088-40de-40a3-a812-d7da7a7b946e" />

Nincs jogosultságunk és elutasítja a rendszer a kérést, mert nem tudja kik vagyunk, nem vagyunk bejelentkezve. 

Ahhoz, hogy tudjuk az EC2 példányunkkal hozzáférni az S3 bucket-hez, létre kell hoznunk IAM role-t. Ennek bemutatása ezen a linken érhető el: [IAM role létrehozása](<./AWS-S3-/IAM role létrehozása/README.md>)

# Csak olvasási role hozzárendelése az EC2-hez.

EC2 instancehoz hozzárendeljük a role-t. 

<img width="1152" height="337" alt="Képernyőfotó 2026-09-30 - 14 39 17" src="https://github.com/user-attachments/assets/84850e7a-3ad2-4b69-b0f2-fe6cfdb5b7dc" />

A listából kiválasztjuk a `csakolvashato` első körben. 

<img width="1369" height="426" alt="Képernyőfotó 2026-09-30 - 14 39 56" src="https://github.com/user-attachments/assets/b39b7bfb-279b-43af-843d-36f11f07ebd7" />

Ha mentettük a beállításokat csatlakozunk az EC2-hez, a korábban leírtak szerint. 

<img width="1379" height="705" alt="Képernyőfotó 2026-09-30 - 14 40 25" src="https://github.com/user-attachments/assets/e9706f1f-d7e5-4caf-8f50-74ae92d33971" />

Először listázzuk a bucket tartalmát: `aws s3 ls s3://s3-alapok-4-599633425313-eu-north-1-an`

<img width="1186" height="394" alt="Képernyőfotó 2026-09-30 - 14 41 28" src="https://github.com/user-attachments/assets/0ef19006-7649-4586-90e2-882128e3bb30" />

Letöltjük az s3-index.html fájlt a következő kéréssel: 
`aws s3 cp s3://s3-alapok-4-599633425313-eu-north-1-an/s3-index.html .
cat s3-index.html`

<img width="1205" height="680" alt="Képernyőfotó 2026-09-30 - 14 44 26" src="https://github.com/user-attachments/assets/59f9209f-0496-4a4f-bf2d-283fd392d037" />

Módosítást végzek el az s3-index.html fájlban és megpróbáljuk visszatölteni a következő utasítással:
`aws s3 cp s3-index.html s3://s3-alapok-4-599633425313-eu-north-1-an/s3-index.html/s3-index.html`

<img width="1385" height="137" alt="Képernyőfotó 2026-09-30 - 15 07 18" src="https://github.com/user-attachments/assets/d74997a3-e31d-4be5-a1f6-a0cd09a409bb" />

Kérés megtagadva, nem sikerült. Az ok nincs jogosultságunk csak olvasási, így nem engedi a feltöltést. 

# Teljes hozzáférés az EC2-nek az S3-hoz. 

Az előzőekben leírtak szerint módosítjuk az EC2 role-t de most a teljes hozzáférést választjuk ki és újra csatlakozunk hozzá. 

<img width="1380" height="403" alt="Képernyőfotó 2026-09-30 - 15 19 07" src="https://github.com/user-attachments/assets/389c493f-9ed8-4431-80b8-608a6ce1fcca" />

A csatlakozás után újra megpróbáljuk feltölteni a s3-index.html fájlt: 
`aws s3 cp s3-index.html s3://s3-alapok-4-599633425313-eu-north-1-an/s3-index.html/s3-index.html/s3-index.html`

<img width="1266" height="329" alt="Képernyőfotó 2026-09-30 - 15 20 45" src="https://github.com/user-attachments/assets/a06d37d9-6f9d-4fd0-8cfa-900d3531d5ac" />

A teljes hozzáféréssel már sikerült a parancsot végrehajtani. 

Az S3 bucketre kattintva láthatjuk is a feltöltött index.html-t. 

<img width="1352" height="442" alt="Képernyőfotó 2026-09-30 - 15 23 25" src="https://github.com/user-attachments/assets/6608c332-946f-4e2b-a893-d31fac052da6" />






