# AWS-S3

AWS S3 **(Simple Storage Service)** egy felhőalapú objektumtároló szolgáltatás, amely nagyon jól skálázható. Az adatokat bucket-ben, "vödör"-ben tárolja. Támogatja a verziózást, így korábbi változatok is megőrizhetőek egy fájlnak és statikus weboldalakat is tárolhatunk rajtuk. 

Az alap S3 bucket létrehozása, a fájl feltöltések, statikus weboldal elhelyezése után bővítjük a lehetőségeket és különböző módon érjük el EC2 példányról és végül Cloudfront használatával a CDN gyakorlását is bemutatom, hogy a statikus weboldalunk elérhetőségének késleltetését csökkentsük. 

### Tartalom
---
1. [S3 - Bucket létrehozása - alap](<./Bucket létrehozása/README.md>)
3. [S3 - Bucket létrehozása - fájl feltöltése](<./Bucket létrehozása -fájl feltöltése/README.md>)
4. [S3 - Verziózás](<./S3 Verziózás/README.md>)
5. [S3 - Statikus weboldal](<./S3 statikus weboldal/README.md>)
6. [S3 fájlok elérése EC2-ről](<./S3 fájlok elérése EC2-ről (IAM role)/README.md>)
7. [IAM role létrehozása](<./IAM role létrehozása/README.md>)
8. [Cloudfront létrehozása](<./Cloudfront létrehozása egy meglévő S3 bucket fölé/README.md>)
