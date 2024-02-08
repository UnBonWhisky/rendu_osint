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

## Informations du fichier `Message.txt`

Lorsque nous ouvrons le fichier, nous avons ce message qui apparaît :  
```
UZUFB XZPSK COYLY PVPDU GCQAT BFMCA ZBZPQ RTEIG TNRVU FPSBH FTJBF QDKMX OYMHF NKNBH LXKJU KKIWL ZVRKN TOFPQ UYKN

#11
```

Le compte twitter référence plusieurs autres message, contenant les #1, #3, #4, #6, #9, #11 (en comptant celui du `Message.txt`)

Les messages sont les suivants :
```
BX ZPK YI GRIHJ DGO EPVDZF XS WDFD UB WPBQCUGT TB BSGJNMDDOZ PU RDESM CEMVPEW 

UVOP LZNWMW XHAC

#1
JYZMG SVDZP RJOVL WOLHI ZAXNZ QSHNG NGTBA XJCMN KRYEG PCQOC VQCXH TMNNU ALSXN UNVCV EJXVE EJ

#1

------------------------------------------------------

ANAR FU LRVMC

XYGR LWWYIZ MXCG

#3
OYLKL QBRXC SUZTX YBDCP GGJGL

#3

------------------------------------------------------

IMFIV OGHDU HA JLZIO XTUON KOJA GIE AWB NQGRJ

CVUV IOEOLF MVDO

#4
NXQYR JZBTB OUHBQ GDRBJ GGTZN FANPB XGSHF OJIOY KPRDU OFWRZ Q

#4

------------------------------------------------------

QI FCYIK DX UFBWPTDI JI FVM

XYLA QAHFMS TRLF

#6
CW MWNHE WI XQMUPECS CP TLJ TZWK JYBBJM NYHL

#6

------------------------------------------------------

ED HWXMPFEW GSABLWBH YJ CNDXCO

RJGR HDUSDU EOUX

#9
TXJNH EPBEY GPIZA QAHBY YSDID QUSCC UKOXY PBXWW

#9

------------------------------------------------------

UZUFB XZPSK COYLY PVPDU GCQAT BFMCA ZBZPQ RTEIG TNRVU FPSBH FTJBF QDKMX OYMHF NKNBH LXKJU KKIWL ZVRKN TOFPQ UYKN

#11
```

Sur le compte twitter, à l'aide de [archive.is](https://archive.is/), nous pouvons voir un post supprimé qui est [celui-ci](https://archive.is/rYvCL#selection-423.28-423.51).  
Son contenu est le suivant :
```
Utilisez le mot de passe de lolcatzx@googlemail.com pour chiffrer vos messages

Vive Cipher Catz !

#14
```

Sur le site IntelligenceX, on a pu trouver le mot de passe en question [sur ce lien](https://intelx.io/?did=b68c4f19-468d-4842-8684-84b7893465ec) qui est `Zerstoren`.

Nous pouvons donc maintenant déchiffrer l'archive avec ce mot de passe.

---

## Contenu de l'archive

L'archive contient une machine Enigma ainsi qu'un tableau.

![Enigma-plugboard](https://github.com/ffouqueray/rendu_osint/assets/65244389/d8252fa4-b213-4761-a504-d5611faa388d)
![carnet](https://github.com/ffouqueray/rendu_osint/assets/65244389/6d605536-8dd4-442f-8958-5894a66f87c5)

Après avoir décodé le message du #11, le message clair est `il faut plus de discretion je propose d'utiliser les canaux de discussion de la societe forsetty vive cipher catz`.

Un autre [compte twitter](https://twitter.com/Forsetty_) existe sous ce nom.

[https://forsetty.com](https://forsetty.com) renvoie sur la page d'accueil OVH.

Un des records DNS de ce domaine est un TXT contient le message "It's not LEET"
