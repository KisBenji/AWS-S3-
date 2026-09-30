# Role létrehozása a Identity and Access Management (IAM) felületen

<img width="1092" height="237" alt="Képernyőfotó 2026-09-30 - 14 14 37" src="https://github.com/user-attachments/assets/d0ef18ca-cbf4-4f9c-ba4d-4f1dc4e59073" />

## Csak olvasási jogosultság létrehozása

Az IAM management felületére belépve a Create Role gombra kattintva elkezdhetjük konfigurálni a szerepkört. EC2-t választjuk, hiszen majd hozzá fogjuk rendelni a role-t.

<img width="1381" height="762" alt="Képernyőfotó 2026-09-30 - 14 15 33" src="https://github.com/user-attachments/assets/44f2731f-d528-4b17-98b2-38bbaf93413e" /> 

A legördülő oszlopból tudjuk kiválasztani milyen szerepkört engedélyezünk. Itt az s3 read only, tehát csak olvasást engedélyező role-t kiválasztjuk. 

<img width="1390" height="517" alt="Képernyőfotó 2026-09-30 - 14 16 12" src="https://github.com/user-attachments/assets/7b87b60f-6d9d-4360-ab67-7fc638d80700" />

Ezután elnevezzük a szerepet: <mark>csakolvashato</mark> 

<img width="1389" height="414" alt="Képernyőfotó 2026-09-30 - 14 16 40" src="https://github.com/user-attachments/assets/ddc66428-4809-42b3-9659-01d8541d225d" />

A Create Role gombra kattintva létre is jön a role, amit most már hozzá rendelhetünk az EC2 példányhoz. 

## Teljes hozzáférési jogosultság létrehozása

A felületen a korábbi lépéseket használva konfigurálunk egy másik role-t is, aminek a teljes hozzáférést engedélyezzük.

<img width="1083" height="511" alt="Képernyőfotó 2026-09-30 - 14 17 22" src="https://github.com/user-attachments/assets/45700e27-c434-40f9-880d-ced082f93749" />

