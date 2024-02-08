# rendu_osint

Il nous a été donné une archive zip avec plusieurs fichiers, cette archive est chiffrée avec le mot de passe `osint`.

L'archive est disponible sous `Data.7z`

---

Après extraction de l'archive, nous obtenons 2 fichiers txt, 1 archive `Random.7z` et une image d'un emplacement google maps.

---

## Récupération de l'emplacement avec la photo

Après avoir ouvert l'image suivante :  

![localisation1](https://github.com/ffouqueray/rendu_osint/assets/65244389/b75f23bc-8232-464d-a28f-f66906725660)

Nous pouvons apercevoir Carbon Health.

En utilisant google image, nous avons pu retrouver l'emplacement de ce batiment, puis nous sommes déplacés jusqu'à San Francisco.

L'emplacement exacte de la capture est de [cet endroit](https://www.google.com/maps/@37.7765558,-122.4176851,3a,75y,34.67h,91.57t/data=!3m6!1e1!3m4!1sICbR6SZDwWJeTubUvMoMjA!2e0!7i16384!8i8192?entry=ttu).

---

## Récupération des metadata de l'image

En utilisant [exiftools](https://exif.tools/) On peut remarquer certains champs dans les metadata comme les Copyrights ou encore l'Owner :

![image](https://github.com/ffouqueray/rendu_osint/assets/65244389/dc947ee3-f6c4-43e5-9420-a363803129b4)

Avec ces informations, nous avons donc l'emplacement de `Twitter` ainsi qu'un Owner qui est `CipherCatz`.  
En recherchant ceci sur twitter, nous trouvons donc le compte de [Cipher Catz](https://twitter.com/CipherCatz)

---

