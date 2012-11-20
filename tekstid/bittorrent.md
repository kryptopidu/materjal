Bittorrent on levinuim failijagamiseks mõeldud P2P-võrgu ehk võrdõigusvõrgu protokoll. Kuna protokoll jaotab failid osadeks, mida eri torrenti (protokolli rahvapärane nimetus) kasutajad hajutatult üles ja alla laadivad, siis on sellisel viisil failide levitamine raskesti tõkestatav. Sel põhjusel kasutavad torrenteid nt nii WikiLeaks kui ka netipraadid. Tavakasutaja jaoks on see aga mugav vahend teha oma suured failid kiiresti avalikult kättesaadavaks ilma ise serveriressurssi panustamata.

Torrenti turvaliseks kasutamiseks on vaja tunda selle omadusi:

  - Torrenti kaudu failide hankimise käigus kasutaja üldjuhul ühtlasi ise jagab neidsamu faile teistele kasutajatele
  - Failide jagajate identiteet on üldjuhul tuvastatav

Seetõttu ei tohiks torrentite kasutajad luua endale illusioone, et nad tegutsevad oma privaatsfääris ega ole jälgitavad. Jälgimise välistab piisavalt suure kindlusega ainult anonümiseerimisteenuse kasutamine, mis on tavaliselt realiseeritud proksi või VPN kujul. Need teenused on üldjuhul tasulised (vt täpsemalt vastava töötoa materjalidest). On olemas meetmeid jälgimise tõenäosuse mõningaseks vähendamiseks (ühenduste krüptimine ja portide juhuslikustamine, jälgijate blokeerimisnimekirja kasutamine), kuid nendele ei saa privaatsuse tagamisel loota.

Torrentite loomine ja allalaadimine
===============================

Torrenti loomine on valikule kasutaja arvutis olemas olevatele failidele krüptoräside loomine ja nende talletamine faili. Sellise torrentifaili abil saab faile seejärel "jagada", st torrentivõrgu kasutajad saavad neid torrentifailis äratoodud krüptoräside alusel orienteerudes alla ja üles laadida.

Kasutame näidiseks avatud lähtekoodiga Bittorrenti klienti Deluge [http://deluge-torrent.org/].

  - Vali failimenüüst torrenti loomine
  - Vali fail(id), mida soovid selle torrentiga jagada
  - Salvesta torrentifail enda valitud kataloogi
  - Vali failimenüüst torrenti lisamine
  - Vali lisamiseks torrenti-fail, mille just salvestasid

Torrenti jagamiseks tuleb loodud torrentifail edastada allalaadija(te)le. Faili võib edastada otse (saata meiliga, panna kodulehele üles jne), aga on ka spetsiaalsed järjepidajad (ingl k *tracker*), mis peavad arvestust torrentite kvaliteedi jpm üle ja aitavad kaasa nende levitamisele. Tuntuim neist on ilmselt The Pirate Bay [https://thepiratebay.se/].

Torrentis kirjeldatud failide allalaadimiseks tuleb lihtsalt torrentikliendiga avada saadud torrentifail:

  - Vali failimenüüst torrenti lisamine
  - Vali torrentifail ja lisa see
  - Oota, kuni torrenti poolt kirjeldatud failid on alla laaditud (kuna torrentivõrk on hajus, siis võib olla vaja oodata, kuni soovitud failid üles leitakse; kui pole ühtki parajasti torrentivõrku sisselogitud kasutajat seda faili jagamas, siis jääb fail kättesaamatuks)
  
Torrenteid saab jagada ka andes torrentifaili asemel edasi selle faili krüptoräsi (ingl k *hash*). Selle alusel leiab torrentiklient ise üles soovitud torrentifaili ja laadib esmalt alla selle ning seejärel ka torrentiga viidatud failid. Paljud torrentikliendid kasutavad räsi edastamiseks "magnetlingi" (ingl k *magnet URI* jt) formaati, Deluge'i puhul tuleb räsi kopeerida kasutajaliidesest:

  - Vali kasutavate torrentite nimekirjast torrentifail
  - Vali alt infopaneelilt detailide vahekaart
  - Märgi ära kood pealkirja "Hash" järel, tee hiire paremklõps ja vali "Kopeeri" (räsi abil allalaadimiseks faili torrenti lisamine ja sisestada kopeeritud räsi vahekaardile "Infohash")

Õiguslikud küsimused
==================

Kuigi Bittorrent võib tavakasutajale seostuda illegaalse failivahetusega, siis tegelikult on see neutraalne andmesideprotokoll, mida võib kasutada mistahes eesmärgiks. Torrentivõrgu hajutatuse tõttu peavad infoühiskonna vabaduste eest võitlejad seda oluliseks komponendiks vaba infovahetuse tagamisel ja seda protokolli täiendatakse jätkuvalt. Eri maade piraadiparteid kaitsevad seisukohta, et ilma ärilise eesmärgita failide jagamine torrentivõrgus peaks olema seadustega lubatud.
