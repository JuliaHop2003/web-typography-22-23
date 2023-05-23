# Web Typography, 2020/2021

Als je doof bent, of als je om een andere reden geen geluid kunt horen, dan mis je veel informatie als je een film kijkt. Knisperende voetstappen, langzaam aanzwellende muziek, nerveus getik op een deur, je hoort het natuurlijk allemaal niet. Nu bestaat er zoiets als *closed caption*, wat een type ondertiteling is waarbij ook dingen als omgevingsgeluiden en de muziek beschreven worden. Hierdoor krijgt een kijker die informatie wel binnen.

Alleen wordt die auditieve informatie nogal neutraal beschreven. Het geluid van huilend persoon zou bijvoorbeeld beschreven kunnen worden als *snikgeluid op de achtergrond*. En iemand die lacht zou geschreven kunnen worden als *iemand lacht.* Heel neutraal, bijna zakelijk, en bovendien allebei in precies hetzelfde neutrale lettertype. Terwijl het toch echt over twee heel verschillende emoties gaat. 

Dat kan visueel sterker. 

En dat gaan jullie doen.

## Leerdoelen

- Je kan de kennis over vormgeving die je hebt opgedaan tijdens de minor technisch toepassen met behulp van CSS
- Je kan verborgen nuance uit een audiotrack overtuigend vertalen naar visuele (typografische) beelden
- Je kan je typografische keuzes onderbouwen.
- Je hebt de exclusive design principles gebruikt.

## Oplevering

Je levert een werkende versie op, gemaakt met HTML, CSS en JavaScript. Deze staat op Github. In een duidelijke readme documenteer en onderbouw je je ontwerpkeuzes. Je developmentgeschiedenis is terug te vinden op GitHub.

Je levert ook een *screen recording* met audio op van je fragment. Dit is een video van de definitieve versie, gemaakt van jouw browserscherm.

De beoordeling is mondeling en volgt [de rubric uit het beoordelingsformulier](web-typografie-beoordeling.pdf).

## Typografische restricties

Je *moet* een van deze twee opties kiezen, en je keuze moet je onderbouwen. In je readme staat een uitleg over je overwegingen om de ene of de andere restrictie te kiezen.

### Optie 1: Systeemfont

De eerste optie is dat je gebruik maakt van het zogenaamde *systeemfont* van degene die naar jouw werk kijkt. Dit font verschilt per operating system, en het verschilt soms zelfs per versie van het operating system. Het is ook aan te passen door de gebruiker zelf. 

Je hebt dus geen controle over welk lettertype er precies gebruikt wordt. Het levert dus een onzeker, en beperkt typografisch palet op. Je hebt geen *light* versies, of *extrabold*. En ook geen serif en sans-serif versie van dezelfde familie. In dit geval heb je alleen de beschikking over normal, **bold** en _italic_. Dit heeft natuurlijk ook zijn voordelen!

### Optie 2: Brenner

Je kan er ook voor kiezen om gebruik te maken van de complete Brenner familie. Dit is een zeer uitgebreid en uiterst flexibel font. [Hier kan je je verdiepen in dit font](https://www.typotheque.com/blog/brenner_an_unusual_typeface_family_with_distinct_voices). Als je kiest voor dit font dan heb je de beschikking over een *sans serif*, een *condensed*, een *serif*, een *monotype*, een *slab*, een *display* en een *script* versie. En veel van deze versies hebben varianten van *light* tot *bold*, en allemaal zowel *bold* als *italic*.

Met Brenner zijn er natuurlijk veel en veel meer mogelijkheden dan met systeemfonts. Dat kan zowel een voordeel als een nadeel zijn. 

Voor een overzicht, zie [de brenner.pdf](brenner.pdf).

## Het fragment

Ik heb een fragment voorbereid. Het gaat om twee scenes uit *Blade Runner 2049*. De captions staan in de HTML, en ze verschijnen in sync met de video. [Kijk maar](closed-captions/index.html).

### De captions

De captions staan in de html, in het bestand index.html. Je kan aan elke paragraaf eventueel een of meer classes toevoegen. Bijvoorbeeld `voice1` of `voice2 soft`. Classes voeg je handmatig toe in de html.

Met JavaScript worden er een paar dingen extra gedaan: 

- er wordt aan elke paragraaf een unieke class toegevoegd (`p0`, `p1`, etc)
- Elk woord wordt in een aparte `span` gezet. Hierdoor kan je elk woord apart stylen, en eventueel ook [na elkaar laten verschijnen](https://github.com/cmda-minor-vid/web-typography-18-19/blob/master/closed-captions/css.css#L41).

### Tijdens het afspelen

Tijdens het afspeelen wordt er een class `on` op de caption gezet als hij moet verschijnen, en een class `off` als hij klaar is. *Zowel class `on` als class `off` blijft op de caption staan!*

De timimg van de captions kan je aanpassen in [closed-captions/captions.js](closed-captions/captions.js).

Er verschijnen ook classes op de body op momenten dat er geluiden worden afgespeeld, zoals `sound1` en `sound2`. Je kan geluiden toevoegen in [closed-captions/sounds.js](closed-captions/sounds.js).

*let op,* de geluiden zijn niet compleet, dit zal je zelf moeten aanvullen.

## Een eigen fragment (afgeraden, uitgebreide onderbouwing is nodig)

Je kan er ook voor kiezen om een eigen, *beter* fragment te gebruiken. Dit wordt afgeraden. De tijd die je besteedt aan het zoeken naar dat fragment kan je beter besteden aan het werken aan de opdracht. Bovendien blijkt dat er vaak fragmenten worden gekozen die niet goed voldoen aan de opdracht. Als je een ander fragment kiest dan *moet* je dit goed onderbouwd voorleggen aan je docent. De deadline hiervoor is vrijdagochtend in de eerste week.

### Waar moet je op letten bij het kiezen van een eigen fragment.
Lees de opdracht nog eens goed door. Waar gaat het ook al weer precies om? 

Voor een goede onderbouwing van je keuze voor een ander fragment moet je deze vragen in elk geval beantwoorden:

- Welke informatie zit er in de audio die echt niet zichtbaar is?
- Welke rol speelt de audio in het fragment?
- Werkt de scene nog zonder geluid?
- Waarom is dit fragment beter dan het aangeboden fragment?

Je kan dan de nodige HTML en JavaScript genereren door gebruik te maken van [caption generator](https://cmda-minor-vid.github.io/web-typography-18-19/generator/) (in Google Chrome). 

Als je de closed captions wil bewerken dan kan je een tool zoals [Amber Script](https://www.amberscript.com/en) gebruiken. Daar kan je exporteren als `.srt`, en die kan je weer door de generator halen.

### Ontwerpkeuzes.
Bij het eerste geluid moest ik denken aan een knop die wordt ingedrukt door iemand waarna je een soort alarmgeluid hoort, dus daarom heb ik ervoor gekozen om een rode knop te visualiseren met een dropshadow eromheen als 'feedback' dat de knop wordt ingedrukt.

Het tweede geluid is een soort van sirene, dus daarom heb ik een blauwe sirene gevisualiseerd door de video rond te laten draaien en de kleur te laten faden van blauw naar lichtblauw. In het echt draait het blauwe licht/de sirena namelijk ook rond.

Het derde geluid is een trillend en een beetje een duister geluid, dus daarom heb ik de achtergrond donkergrijs gemaakt en laat ik de video trillen.

Het vierde geluid is een soort van laser geluid die aan het eind iets harder klinkt, dus daarom laat ik de video inzoomen en heb ik een laserstraal gevisualiseerd door het te laten flikkeren.

Bij het vijfde geluid is er een soort van angstig geluid en blauw is de kleur van angst, dus daarom heb ik voor die kleur gekozen en ik laat de video bouncen om aan te geven dat Skinjob's hart tekeer gaat van spanning/angst.

Tijdens de baseline test begin ik met verschillende kleuren die langzaam in elkaar faden om aan te geven dat 'Skinjob' in een sessie/eigen space zit. Wanneer de piep harder wordt beginnen de kleuren wat sneller te flikkeren en op het eind flikkert het nog veel sneller en ziet het er spacend uit door al die kleuren. Ook wordt langzaam de video groter, dus wanneer het geluid stopt en er een stilte valt, gaat de video weer terug naar zijn eigen grootte.

Op het eind zie je een soort van herinning van een eerdere test, maar die test ging fout, dus daarom gaat de kleur van wit naar zwart om aan te geven dat de test op het eind fout gaat en de video klaar is.

Qua tekst heeft iedere stem een eigen lettertype. Voice1 klinkt bazig en heeft een normale toonhoogte, dus daarom heeft die het normale Brenner font met de schreven eraan om het een wat duurdere/bazige uitstraling te geven. Voice2 oftewel Skinjob praat een beetje zonder emotie, maar heeft wel een normale toonhoogte, dus ik heb Brenner Sans gegeven, omdat Brenner Sans geen schreven etc. heeft. Voice3 klinkt agressief, maar heeft een lage toonhoogte, dus daarom heb ik Brenner Light gekozen, omdat Brenner Light als agressief kan worden gezien vanwege alle schreven en de light versie als zacht praten kan worden ervaren. Dan is er ook nog een voice5. Voice5 klinkt een beetje computerachtig, dus daarom heb ik gekozen voor Brenner Mono, omdat mono wordt gebruikt voor bijvoorbeeld coderen en daarom ook computerachtig is. 

Op het eind zijn de lettertypes hetzelfde, alleen is alles schuingerukt om aan te geven dat dit een herinning/oud fragment is.

1e voortgangsgesprek:
Tijdens het eerste voortgangsgesprek had ik nog niet heel veel, maar kreeg ik wel alvast te horen waar ik op kan letten, zoals dat bijvoorbeeld "Fuck off, Skinjob!" best wel zacht wordt gezegd en dat je moet letten op dat je de video visualiseert en niet de tekst. Dus dit heb ik vermeden toen ik verder ging met mijn proces.

2e voortgangsgesprek:
Tijdens het 2e voortgangsgesprek heb ik de vraag gekregen of de kleuren niet te fel zijn tijdens de 'post-traumatic baseline test'. Na deze feedback heb ik de kleuren wat donkerder gemaakt, omdat dat beter past bij de vibe van de film. Ook blijft ondanks de donkere kleuren het knipperende effect nog hetzelfde.