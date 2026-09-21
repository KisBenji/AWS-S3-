# S3 statikus weboldal

A Bucket elnevezése: <mark>s3-alapok-4<mark>

<img width="1292" height="749" alt="Képernyőfotó 2026-09-21 - 14 16 19" src="https://github.com/user-attachments/assets/1828d92b-f43e-4523-8ff3-b31d89180ecc" />

A publikus hozzáférés tiltását engedélyezzük, hogy elérhető legyen a weboldal.

<img width="1442" height="561" alt="Képernyőfotó 2026-09-21 - 14 17 37" src="https://github.com/user-attachments/assets/758c11bd-0476-4e39-9081-2098cf4299db" />

<img width="1226" height="540" alt="Képernyőfotó 2026-09-21 - 14 17 52" src="https://github.com/user-attachments/assets/96ee79b7-5605-4127-9d64-88b99c229262" />

A `Bucket policy`-t konfiguráljuk és JSON fájl-t töltünk fel. Itt már látszik a Bucket neve is


<img width="1276" height="598" alt="Képernyőfotó 2026-09-21 - 14 22 22" src="https://github.com/user-attachments/assets/b75e2117-5588-40ab-a76b-901b7c0e10df" />

Ezután feltöltöttem egy `s3-index.html` és `s3-error.html` fájl-t a Bucket-be.

<img width="1279" height="748" alt="Képernyőfotó 2026-09-21 - 14 24 47" src="https://github.com/user-attachments/assets/79bee356-bb2f-4f40-8ccc-9651c48a5064" />

Ezután elérhetővé `Enable` Static website hosting lehetőséget és megadjuk a korábban feltölött fájlok nevét.

<img width="1255" height="750" alt="Képernyőfotó 2026-09-21 - 14 28 59" src="https://github.com/user-attachments/assets/7264d8d4-4e93-4fb4-8cd3-f01c7d9976f6" />
