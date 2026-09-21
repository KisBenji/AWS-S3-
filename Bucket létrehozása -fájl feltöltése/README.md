# Bucket létrehozása - fájl feltöltése 
### Globálisan egyedi névvel

A korábbiakhoz hasonlóan a console felületén az S3-ra kattintva - `Create bucket` elkezdjük konfigurálni. 

Név: <mark>s3-alapok-1<mark>

<img width="1276" height="727" alt="Képernyőfotó 2026-09-21 - 13 59 46" src="https://github.com/user-attachments/assets/1fd6d133-eb12-4ebd-b78d-ee62032fe8fb" />

Itt is egyelőre default beállításokat hagyunk meg, hogy ne legyen publikus az internet felől.

<img width="1455" height="399" alt="Képernyőfotó 2026-09-21 - 13 59 53" src="https://github.com/user-attachments/assets/9d4c8228-6797-4f5a-adaa-c7edfdb40c9d" />

A létrehozott bucket-ba feltöltünk egy dokumentumot

<img width="1273" height="737" alt="Képernyőfotó 2026-09-21 - 14 00 59" src="https://github.com/user-attachments/assets/a189ad4d-57fc-4d5b-8791-9a7f886d0928" />

A `Properties` kattintva láthatjuk az fáljhoz tartozó URL-t 

<img width="1362" height="653" alt="Képernyőfotó 2026-09-21 - 14 01 16" src="https://github.com/user-attachments/assets/70db4036-a68e-4e59-a75c-e19ce6498768" />

Rákattintva a következő kép fog megjelenni, ami teljesen normális, hiszen nem engedélyeztük a publikus hozzáférést. 

<img width="916" height="201" alt="Képernyőfotó 2026-09-21 - 14 01 24" src="https://github.com/user-attachments/assets/fa599d70-4909-45ae-979d-ff31ef269f2e" />

### Account szinten egyedi névvel

Az első lépések megegyeznek S3 - `Create bucket` és megkezdjük a konfigurációt.

Ennél a pélánál egyedi azonosítót választunk, amelyet az AWS account egyedi adatait és a régiót is tartalmazza.

<mark>s3-alapok-2<mark>

<img width="1149" height="670" alt="Képernyőfotó 2026-09-21 - 14 06 03" src="https://github.com/user-attachments/assets/06b20d26-c5bb-4b7b-b4c1-88e6a8c64e41" />

A többi beállítást default hagyjuk, ami azt jelenti továbbra is korlátozzuk a publikus hozzáférést.

<img width="1417" height="415" alt="Képernyőfotó 2026-09-21 - 14 06 52" src="https://github.com/user-attachments/assets/14b83f4c-312f-4254-9dd0-92626332ad78" />

A létrehozott Bucket-ba feltöltöttem újból egy képet:

<img width="1272" height="750" alt="Képernyőfotó 2026-09-21 - 14 07 26" src="https://github.com/user-attachments/assets/9b720b14-43ca-416e-ae62-b41cea464f6f" />

Az objektum URL-re kattintva ellenőrizzük, hogy elérhető-e. 

<img width="1179" height="586" alt="Képernyőfotó 2026-09-21 - 14 07 33" src="https://github.com/user-attachments/assets/5aeed61f-6050-4387-8934-86544a96d4c2" />

Szintén megtagadja a hozzáférést, hiszen az alap beállításokat használtuk ebben az esetben is.

<img width="951" height="159" alt="Képernyőfotó 2026-09-21 - 14 07 40" src="https://github.com/user-attachments/assets/db6ea7a9-20a2-4abe-b0e8-cbe2c25f736f" />

További fájlokat töltöttem fel ebbe a Bucket-ba is. 

<img width="1461" height="640" alt="Képernyőfotó 2026-09-21 - 14 08 53" src="https://github.com/user-attachments/assets/69afd613-3953-4d61-8af7-334dcde24931" />
