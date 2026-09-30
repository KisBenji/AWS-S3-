# A tartalmunk már a bucketben van így könnyedén a console segítségével létre tudunk hozni egy distribution-t.

Keresőbe beírjuk a Cloudfront alkalmazás nevét és belépve a Create distribution indításával megkezdjük a konfigurálást

<img width="1393" height="307" alt="Képernyőfotó 2026-09-30 - 15 36 03" src="https://github.com/user-attachments/assets/1ac5dcad-918a-4fac-9b2a-3deea0e1b020" />

Elnevezzük ami a példa kedvéért: <mark>s3-distribution</mark>

<img width="1338" height="701" alt="Képernyőfotó 2026-09-30 - 15 36 38" src="https://github.com/user-attachments/assets/b257ce5b-db16-48e1-bc20-0af7197b4640" />

Az origin esetén kiválasztjuk az S3-t

<img width="1389" height="714" alt="Képernyőfotó 2026-09-30 - 15 37 10" src="https://github.com/user-attachments/assets/c7d4d9e3-0be6-4cbc-8715-df2744a31ab6" />

Hozzárendeljük a mi saját statikus weboldalunkat tartalmazó S3 bucketet:

<img width="927" height="537" alt="Képernyőfotó 2026-09-30 - 15 36 59" src="https://github.com/user-attachments/assets/55556565-5e44-4eb7-8ee9-6172b4546730" />

Ha a public website hosting engedélyezve van a bucketen, a CloudFront a kéri hogy annak az URL-jét (Static endpoint) használd: "This S3 bucket has static web hosting enabled. If you plan to use this distribution as a website, we recommend using the S3 website endpoint rather than the bucket endpoint." 

<img width="1389" height="714" alt="Képernyőfotó 2026-09-30 - 15 37 10" src="https://github.com/user-attachments/assets/99c71eea-1065-4660-a872-7f2f056043e3" />

