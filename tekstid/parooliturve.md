Paroolihaldus
=============

Üheks kõige elementaarsemaks digitaalse turvalisuse alustalaks on parool e. salasõna. Turvaline parool peaks olema piisavalt pikk (15+ sümbolit), sisaldama nii väike- kui suurtähti ning soovitavalt ka numbrimärke ja/või teisi levinud sümboleid. Targalt valitud parool ei tohiks sisaldada kergesti arvatavaid elemente nagu näiteks omaniku sünnikuupäev, pereliikmete nimed ning levinud tsitaate või muid elementaarseid sõnapaare mida on sõnaraamat-tüüpi rünnakutega lihtne lahti murda.

Sellised ranged nõudmised salasõnale, inimeste mugavus ja suur salasõnapõhist autentimist nõudvate teenuste hulk tekitavad olukorra kus kiusatus on kasutada samu või väga väikeste variatsioonidega paroole erinevate kontode puhul. Kui nüüd üks nendest paroolidest sattub pahalase kätte, sattuvad ohtu ka paljud teised turvatud kontod. 

Antud olukorrale pakub lahenduse paroolihaldustarkvara, mis hoiustab kõik paroolid ühtses krüpteeritud andmebaasifailis, millele kasutaja pääseb ligi hoolikalt valitud peaparooliga. Üks selline levinud tarkvaralahendus on avatud lähtekoodiga [KeePass][1], mis on kasutatav nii Windows, Mac OS X ja Linuxi operatsioonisüsteemidel. KeePass'i parooliandmebaase saab avada ka nutitelefoni jaoks loodud rakendustega: [KeePassDroid][2] (Android) ja [MiniKeePass][3] (iPhone).

KeePass toetab hetkel *Global Auto-Type* funktsiooni abil automaatset paroolide sisestamist interneti lehitseja ja muude programmide väljadele vaid Windowsi keskkonnas. Linuxi all soovitame kasutada [KeePassX][1] rakendust. Loodetavasti toetab KeePassX lähitulevikus *Global Auto-Type* funktsiooni ka Windows ja Mac OS X versioonides.


KeePass'i seadistamine ja kasutamine (Windows'is):
-------------------------------------------------

1) Laadige KeePass Classic versioon alla aadressilt [http://keepass.info/download.html](http://keepass.info/download.html), paigaldage oma arvutisse teile meelepärasesse kataloogi ja käivitage. Classic versiooni soovitame kasutada selle pärast, et see toetab ainult KeePass x.1 tüüpi andmebaasifaili formaati, mis ühildub nii KeePassX kui ka nutitelefonidele mõeldud rakendustega.

2) Loome uue andmebaasifaili valides *File* menüüst *New* ja sisestage turvastandardeid järgiv peaparool. See on ainuke parool, mida te edaspidi peate meeles pidama.

3) Valige *File* menüüst *Save As* ja valige oma paroole säilitavale andmebaasifailile sobilik nimi ja kataloog.

4) Paneme paika soovituslikud seaded (puuduvad linnukesed) menüüst *Tools* -> *Options*:

   - Security
      - Lock workspace when minimizing the main window
      - Lock workspace when locking Windows, switching user or sleeping
      - Lock workspace after following idle time (seconds): 1800 (30 min)
   - Interface (GUI)
      - Minimize to tray instead of taskbar
      - Close button [X] minimizes the main window instead of terminating the application
   - Advanced
      - Integration
         - Start KeePass at Windows startup (for current user)
         - Start minimized and locked
      - Start and Exit
         - Start minimized and locked
         - Automatically save when closing/locking the database
      - Auto-Type nupp all paremal -> Global auto-type hot key: Ctrl + Alt + P

Vajuta OK.

5) Uute paroolide lisamine.

Valige vasakult tulbast sobiv kategooria ja klikake ikooniribal rohelise noolekesega võtmeikooni või valige menüüvalikus *Edit* -> *New Entry*. Avanevasse aknasse sisetage sisse logitava kodulehe tiitel, kasutajanimi ja parool (uut parooli saab genereerida ka sisseehitatud võtmemärkidega  nupult avaneva parooligeneraatori abil). Vajutage OK.

6) Testime kas uus parool töötab, minnes internetilehitsejas kodulehele, mille autentimise parooli me just lisasime. Viime hiirekursori kasutajanime sisestusväljale ja vajutame seadetes eelnevalt defineeritud *Auto-Type* klahvikombinatsiooni (Ctrl + Alt + p).


KeePassX'i seadistamine ja kasutamine (Linux'is):
------------------------------------------------

1) Laadige KeePassX alla aadressilt [https://www.keepassx.org/downloads] (https://www.keepassx.org/downloads), paigaldage oma arvutisse teile meelepärasesse kataloogi ja käivitage.

2) Loome uue andmebaasifaili valides *File* menüüst *New Database* ja sisestage turvastandardeid järgiv peaparool. See on ainuke parool, mida te edaspidi peate meeles pidama.

3) Valige *File* menüüst *Save Database As* ja valige oma paroole säilitavale andmebaasifailile sobilik nimi ja kataloog.

4) Paneme paika soovituslikud seaded (puuduvad linnukesed) menüüst *Extras* -> *Settings*:

   - General (1)
      - Show system tray icon
        - Minimize to tray instead of taskbar
        - Minimize to tray when clicking the main window's close button
      - Remember last opened file
        - Start minimized
        - Start Locked
   - General (2)
      - Automatically save database on exit and workspace locking
   - Security
      - Lock database after inactivity of 1800 seconds (30 minutit)
   - Advanced
      - Global Auto-Type Shortcut: Ctrl + Alt + p (Ainult Linuxi all hetkel)
      - Use entries' title to match the window for Global Auto-Type

Vajuta APPLY ja siis OK.

5) Uute paroolide lisamine.

Valige vasakult tulbast sobiv kategooria ja klikake ikooniribal rohelise noolekesega võtmeikooni või valige menüüvalikus *Entries* -> *New Entry*. Avanevasse aknasse sisetage sisse logitava kodulehe tiitel, kasutajanimi, URL link ja parool (uut parooli saab genereerida ka sisseehitatud *Gen* nupult avaneva parooligeneraatori abil). Vajutage OK.

6) Testime kas uus parool töötab, minnes internetilehitsejas kodulehele, mille autentimise parooli me just lisasime. Viime hiirekursori kasutajanime sisestusväljale ja vajutame seadetes eelnevalt defineeritud *Global Auto-Type* klahvikombinatsiooni (Ctrl + Alt + p).


Lisamärkused:
-------------

Paroole sisaldavat krüpteeritud andmebaasifaili on kõige lihtsam sünkroniseerida ja jagada teiste seadmetegega, kasutades [DropBox][5] teenust.

Ärge lisage KeePass(X) andmebaasi elulise tähtsusega paroole - pankade paroole ja oma peamist e-maili konto parooli. See vähendab olulisel määral turvariski kui pahalane peaks mingil põhjusel teie KeePass(X) andmebaasi sisule ligi pääsema.

Viited:

[1]: http://keepass.info
[2]: https://play.google.com/store/apps/details?id=com.android.keepass&hl=en
[3]: https://itunes.apple.com/us/app/minikeepass-secure-password/id451661808?mt=8
[4]: https://www.keepassx.org
[5]: https://www.dropbox.com

