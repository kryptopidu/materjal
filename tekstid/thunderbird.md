Mine: http://www.sk.ee/certs

Laadi alla ja salvesta kettale (jäta asukoht meelde, neid läheb pärast vaja):

  - ESTEID-SK 2007 PEM: http://www.sk.ee/upload/files/ESTEID-SK%202007.PEM.cer
  - ESTEID-SK 2011 PEM: http://www.sk.ee/upload/files/ESTEID-SK%202011.pem.cer

PÕHITEGEVUS TOIMUB SELLES AKNAS
============================

Redigeerimine -> Kontode sätted -> *sinu konto* -> Turvalisus
(Tööriistad -> ...)

TURVASEADMED
===========

Turvaseadmed -> Laadi -> Lehitse...

  - Linux: /usr/lib/onepin-opensc-pkcs11.so
  - Windows: /Windows/system32/onepin-opensc-pkcs11.dll
  - Mac: /Library/OpenSC/lib/onepin-opensc-pkcs11.so

Turvaseadmete haldur kinni vajutades: Sobib

SERTIFIKAADID
============

Kuva sertifikaate -> Sisesta PIN1

Keskused -> Impordi

(asukohast, mille alguses meelde jätsid)

  - ESTEID-SK 2007 PEM -- Usalda seda SK-d e-posti kasutajate identifitseerimisel.
  - ESTEID-SK 2011 PEM -- Usalda seda SK-d e-posti kasutajate identifitseerimisel.

Sertifikaatide haldur kinni vajutades: Sobib

PÕHIAKNAS JÄLLE
=============

  - Digiallkirjastamine -> Vali oma sertifikaat
  - Avaneb dialoog, mis küsib, kas kasutada sama sertifikaati ka krüptimiseks. Võib nõustuda.

  - Krüptimine -> Vali oma sertifikaat


Nüüd peaks saama kirjasid PIN1 abil allkirjastada (see pole digiallkiri õiguslikus mõttes). Kirja kirjutamisel on üleval valik "Turvalisus", kust saab määrata, kas allkirjastatakse või krüptitakse või mõlemat.

Krüptimiseks on vaja lisada Thunderbirdi adressaadi sertifikaat ja krüptida saab ainult saates ametlikule karu.mati@eesti.ee aadressile.

Sertifikadid -> Inimesed -> Impordi

Sertifikaadi saab adressaadi käes või teades isikukoodi järgnevalt:

Digidoc krüpto
=============

Krüpteerida faile -> *suvaline fail* -> Lisa adressaat (all servas väike) -> Isikukood -> Lisa adressaaat -> Sulge -> Vaata üksikasju -> Näita sertifikaati -> Detailid -> Salvesta

Vt lisaks: http://www.id.ee/index.php?id=34232


