Truecrypt
=========

Meil kõigil on arvutis faile, mida teistel pole vaja näha. Lihtne võimalus on panna oma arvuti kasutajakontole parool ja kasutada ekraanilukku, aga mis siis saab, kui teie arvuti varastatkse? Sel juhul pole kasutajakonto paroolist midagi abi, sest vargal on väga lihtne pääseda teile failidele ligi failisüsteemi tasemel ilma et ta peaks teie operatsioonisüsteemi käivitamagi. Selle vastu aitab tähtsate failide või terve kõvaketta krüpteerimine.

Truecrypt [http://www.truecrypt.org] on tasuta vabavaraline tarkvara, mis võimaldab lihtsa vaevaga tähtsaid faile krüpteerida. Vastavalt vajadusele saab krüpteerida erineval tasemel:

  - terve kõvaketas või mälupulk korraga
  - üks või mitu kõvaketta või mälupulga partitsiooni (sh süsteemiketas)
  - vajaliku suurusega failide konteiner (virtuaalne ketas)

TrueCrypt tarkvara toetab nii Windows, Mac OS X kui ka Linux operatsionnisüsteeme. Järgnevas juhendis on näitens kasutatud Windowsi versiooni, kuid teistes operatsioonisüsteemides on TrueCrypt käitumine analoogne.

Krüpteeritud failikonteineri tegemine
-------------------------------------

Kui kaitsmist vajavaid faile on piisavalt vähe, siis on kõige lihtsam ja mõistlikum teha nande jaoks üks krüpteeritud konteiner. Selline konteiner kujutab endast virtuaalset ketast (näiteks *Z:\\* ketas), mille sisu hoitakse tegelikult ühes krüpteeritud failis. Kuna tegemist on üheainsa failiga, siis on seda lihtne ka ühest arvutist teise tõsta ning vajadusel isegi näiteks isikliku ja tööarvuti vahel automaatselt sünkroniseerida, kui see tõsta näiteks Dropboxi  [https://www.dropbox.com/] kausta.

Krüpteeritud failikonteineri loomiseks toimige nii:

  - Käivitage Truecrypt.
  - Valige *Volumes* menüüst *Create New Volume...*
  - Avanenud aknas valige *Create an encrypted file container* ja vajutage *Next*.
  - Valige *Standard TrueCrypt volume* ja vajuage *Next*.
  - Valige, kuhu tahate oma krüpteeritud konteineri fail tekitada ning vajutage *Next*
  - Järgmises aknas saab valida krüpteerimisel kasutatavad šifri- ja räsialgoritmid, aga üldjuhul sobivad vaikeväärtused häst. Vajutage *Next*.
  - Nüüd tuleb hinnata kui palju faile te plaanite selle konteineri sees hoida ja sisestada konteineri mahu ülempiir. Liialt ei maksa siinkohal muretseda, sest alati saab tekitada uue suurema konteineri ning failid lihtsalt sinna üle tõsta. Kui olete sobiva suuruse valinud, vajutage *Next*.
  - Nüüd tuleb valida parool, millega tulevikus konteinerit lahti krüpteerida saab. Seda peab sisestama kaks korda. Nagu ikka, peab parool olema piisavalt keeruline, et keegi teine seda ära ei arvaks, kuid samas peaks see endale meelde jääma. Siinkohal võib valida ka mõne keerulise parooli ning pärast mõnes teises töötoas õppida, kuidas KeePass [http://keepass.info] abil oma paroole lihtsalt hallata :) Parooli asemel või sellele lisaks võib kasutada ka võtmefaile, mille sisu kasutades oskab TrueCrypt siis krüpteerida. Kuna arvutis on faile plaju, siis ei oskagi teised arvata, kui palju ja milliseid faile krüpteerimisel täpselt kasutati ning see toimibki võtmena. Loomulikult peab siis ettevaatlik olema, et valitud failide sisu ise ei muudaks. Kui parool (ja/või võtmefailid) valitud, vajutage *Next*. Liiga lühikese või lihtsa parooli peale võib TrueCrypt kurta. Siis tuleks turvalisem parool valida, aga seda teadet saab ka ignoreerida.
  - Järgmises dialoogis saab valida failisüsteemi (FAT või NTFS). Kui konteinerisse pole plaanis paigutada suuri faile (> 4 GB), siis võib lihtsuse huvides kasutada FAT failisüsteemi. Kui teha linnuke *Dynamic* ette, siis ei tehta konteinerit mitte kohe eelnevalt valitud maksimaalse suurusega, vaid ainult nii suur kui parasjagu tarvis. Kahjuks on sel juhul aga konteineri kasutamine oluliselt aeglasem. Vajutage *Format* ja järgmisena *Exit*.
  - Nüüd peaks taas ees olema TrueCrypt põhiaken. Sealt tuleb nüüd valida *Select File...* ning üles otsida eelnevalt tekitatud konteiner. Valige ülevalt nimekirjast sobiv täht virtuaalsele kettale ja vajutage *Mount*.
  - Avanenud aknas tuleks nüüd sisestada parool ja/või ette näidata võtmefailid ning vajutada *OK*.
  - Failihaldurist on nüüd näha, et valitud tähega on tekkinud uus ketas. ALgselt on see tühi ja sinna tuleks nüüd soovitud faild tõsta.
  - Virtuaalse ketta lahtiühendamiseks avage TrueCrypt, valige nimekirjast täht, mille alla on virtuaalne ketas tekitatud ning vajutage *Dismount*.


Truecrypti krüpteeritud failikonteiner töötab sarnaselt ID-kaardiga failide krüpteerimisele, aga kuna see ühendatakse arvutisse virtuaalse kettana, siis on seda mugavam kasutada ning lisaks ei pea muretsema selle pärast, et peale ID-kaardi sertifikaatide uuendamist ei pääse oma failidele enam ise ka ligi.
