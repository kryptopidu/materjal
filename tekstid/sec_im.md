# Turvaline IM #

## Sissejuhatus ##
See juhend on mõeldud neile, kes tahavad oma veebipõhised vestlused (MSN, Skype, Facebook, Google Talk) turvalisemaks muuta. Turvalisuse all saab eristada kahte taset - võrgu tasemel pealtkuulatavus ja tehniline privaatsus. 

Võrgu tasemel pealtkuulatavus näitab, kas arvutivõrgu administraatorid (nt wifi-punkti operaator, ettevõtte IT osakond) või pahatahtlikud nuhid saavad soovi korral vestlust pealt kuulata, püüdes kinni üle wifi/juhtme liikuvaid andmesidepakette. 

Tehniline privaatsus näitab, kas teenusepakkujal endal (nt Facebook) on soovi või kohtu käsu korral üldse võimalik vestlusi pealt kuulata ja salvestada.

## Miks on turvaline IM keeruline ##
Et saaks tagada täieliku privaatsuse ja sõnumite kõrvalistele isikutele loetamatuse, peab terve vestluse krüpteerima - vestlus muudetakse võtme (nt salasõna) ja matemaatiliste algoritmide abil loetamatuks, nii et selle saavad tagasi loetavale kujule viia ainult teised sama võtit omavad osapooled. 

Esiteks, et süsteem toimiks, peavad mõlemad osapooled kasutama sellist tarkvara, mis suudab vestlusi krüpteerida-dekrüpteerida, muidu üks pooltest näeb ainult loetamatut infot.

Teiseks tuleb kontrollida, et tõesti suudeti luua otseühendus õige vestluspartneriga. Üks ohtlikem ründeviis on see, kui ründaja suudab vestluspartnerite vahelist ühendust kontrollida ja jätta sinu arvutile mulje, et ta suhtleb otse partneri arvutiga ja partneri arvutile mulje, et ta suhtleb otse sinu arvutiga, kui tegelikkuses käib kogu liiklus läbi ründaja arvuti. Sellist rünnet kutsutakse vahendajaründeks (MITM), seda ei saa välistada, aga seda saab tuvastada. 

## Skype ##
Skype on huvitav programm, sest ta krüpteerib kõik vestlused, aga keegi ei tea, kuidas ta seda teeb, sest see on saladus. Igal juhul ei saa skype vestlusi võrgu tasemel pealt kuulata, sest näha on ainult loetamatut krüpteeritud sõnumivahetust. Seega pole avalikud wifi-punktid ja ebaturvalised võrgud mureks. Küsimus on selles, kas kohtud või lihtsalt rikkad osapooled saavad skype'lt vestluste salvestisi "tellida". Kuna skype täpne tööpõhimõte ei ole teada, ei ole võimalik kontrollida, et skype'l ei ole võimalik vestlusi salvestada. 

## Facebook ##
Facebooki chat on ilmselt üks vähim-turvalisi vestlusvõimalusi. Tavajuhul on see mõlemat võrgu tasemel pealtkuulatav ja tehniliselt pealtkuulatav, ehk avalikus wifi-punktis istudes on kogu vestlus kõigile nähtav ja hiljem saab ka facebookist logisi küsida.

Õnneks on võimalik võrgu tasemel pealtkuulamist vältida, lülitades facebooki seadetes sisse HTTPS protokolli (sama tehnoloogia, mida internetipangad kasutavad). Selleks tuleb avada "Account settings" ja "Security" tabis "Secure browsing" sisse lülitada.

Selle vastu, et facebook kõik su vestlused salvestab ja neid pärast huvitatud osapooltega jagab, ei saa midagi teha. Küll aga on võimalik sõnumid ära krüpteerida, et facebook nendega midagi kasulikku teha ei saaks - abiks on järgnevad programmid. 

## Pidgin + OTR ##
Leidub programm Pidgin, millega saab chatida MSNis, Facebookis ja Google Talkis. Sellel on ka OTR (off-the-record) nimeline plugin, millega saab kõik vestlused krüpteerida. Siiski eeldab see, et ka teine pool kasutab sama tarkvara, muidu ta näeb sõnumeid ainult loetamatul kujul.

Pidgini saab tasuta veebist - http://www.pidgin.im ja OTR plugini saab aadressilt http://www.cypherpunks.ca/otr/. Täpsem juhend OTR kasutamiseks on aadressil http://bit.ly/Q3jAZg

Lühidalt tuleb "Tools" menüüs "Plugins" valida ja OTR plugin sisse lülitada. Edasi, iga uue vestluspartneriga tuleb vestlusakna "OTR" menüüst valida "Start private conversation". Kui vestluspartneril on OTR plugin olemas, on edasine vestlus krüpteeritud. Google Talk puhul saab seda näiteks kontrollida GMaili sisse logides ja chat historyt vaadates.

## Jitsi ##
Jitsi on midagi Skype ja Pidgini vahepealset. Tema abil saab chatida, teha heli ja videokõnesi ja kõik on automaatselt krüpteeritud. Lisaks on Jitsi tööpõhimõte väga selge ja avalik, mistõttu saab tagada, et keegi kõrvaline isik tõesti ei saa vestlusi pealt kuulata ega salvestada. 

Jitsi saab downloadida aadressilt https://jitsi.org/ ja kohe käivitamisel saab tema kaudu sisse logida MSNi, Facebook chati ja Google Talki. Kuna chati krüpteerimisel kasutatakse sama tehnoloogiat, mis Pidgini OTRis, siis saab krüpteeritult chatida ka kõigi Pidgin+OTR kasutajatega. 

Nii Jitsi kui ka Pidgini OTR plugin laseb kasutajal ennast vahendajaründe eest kaitsta, kasutades erinevaid kontrollivõimalusi. 

## Viited ##
1. [What is Diffie-Hellman?](https://www.rsa.com/rsalabs/node.asp?id=2248)
2. [Man-in-the-middle attack](http://www.computerhope.com/jargon/m/mitma.htm)
3. [Don't believe the Skype: it may not be as private as you might think](http://www.guardian.co.uk/commentisfree/2012/jul/27/skype-encyption-methods-police-access)
4. [Facebook scans chats and posts for criminal activity](http://news.cnet.com/8301-1023_3-57471570-93/facebook-scans-chats-and-posts-for-criminal-activity/)
5. [A Skype alternative worth its salt: Jitsi](https://apapadop.wordpress.com/2012/07/05/a-skype-alternative-worth-its-salt-jitsi/)

> CC-BY-SA Märt Bakhoff 2012 Krüptopidu
