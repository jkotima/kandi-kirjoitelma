# Ohjelmiston arkkitehtuurisuunnittelu ketterissä menetelmissä

Ohjelmiston arkkitehtuuri on IEEE:n standardin mukaan ohjelmiston perusorganisaatio, joka sisältää järjestelmän osat, niiden keskenäiset suhteet ja suhteet ympäristöön. Määritelmän mukaan arkkitehtuuri ohjaa järjestelmän suunnittelua ja evoluutiota. 

Rational Unified Process määrittelee ohjelmistoarkkitehtuurin joukkona perustavanlaatuisia päätöksiä koskien järjestelmän organisaatiota, rakenteellisia elementtejä, rajapintoja, alijärjestelmiksi jakautumista, arkkitehtuurillista tyyliä ja niin edelleen. RUP:in mukaan arkkitehtuurissa ei olla kiinnostuneita pelkästään rakenteesta ja toiminnasta, mutta myös sen käyttökohteesta, suorituskyvystä, joustavuudesta, uudelleenkäytettävyydestä ja ymmärrettävyydestä. Arkkitehtuurissa pitäisi ottaa huomioon taloudelliset ja teknologiset rajoitteet.

Nykyään suosioon nousseita ketteriä menetelmiä, kuten Scrumia ja Extreme programmingia, yhdistää iteratiivinen ja inkrementaalinen elinkaari, pienissä erissä tapahtuvat julkaisut, yhtenäinen tiimi sekä ominaisuus- tai tuotebacklogiin perustuva julkaisusuunnitelma. Olennaista on myös pyrkiminen prosessin yksinkertaisuuteen ja sopeutuminen vaatimusten muutoksiin. Eri ketterien menetelmien kuvaukset ei tyypillisesti kerro mitään arkkitehtuurista. Esimerkiksi Scrumiin ei ole määritelty, kuinka arkkitehtuurisuunnittelu tulisi toteuttaa, Extreme Programmingissa (XP) arkkitehtuurin rakentumista määrittelee ainoastaan järjestelmämetafora (system metaphor).

Perinteisessä ohjelmistotuotannossa, kuten vesiputousmallissa, ohjelmistoon liittyvä suunnittelu tapahtuu tyypillisesti ennen varsinaista sovelluksen toteutusvaihetta.
Tämä Big Design Up-Front (BDUF) -käytäntö sisältää myös ohjelmiston arkkitehtuurin suunnittelun.

Ketterän ohjelmistokehityksen periaatteet ovat epäsuhdassa arkkitehtuuriperustaisen ohjelmistosuunnittelun kanssa. Ketterän manifestin mukaan esimerkiksi muutokseen reagoimista pidetään tärkeämpänä kuin tarkkojen suunnitelmien noudattamista. Halutaan minimoida kaikki turha työ, sillä arkkitehtuuriin saatetaan joutua tekemään muutoksia myöhemmässä vaiheessa. Ketterässä kehityksessä ihanteena on, että päätökset pyritään tekemään mahdollisimman myöhäisessä vaiheessa: mitä myöhemmässä vaiheessa päätökset tehdään, sitä enemmän tietoa on hyödynnettävissä päätösten tueksi. Asiakkaalle arvoa tuottava ohjelmiston ominaisuuksien nopea tuottaminen nähdään tärkempänä asiana kuin "ajan tuhlaaminen" tarkkaan suunnitteluun ja dokumentaatioon. 

Abrahamsson et al. artikkelissa Agility and architecture: Can they coexist? (2010) mukaan suurin vastakkainasettelu on ketterän kehityksen sopeutumismentaliteetin ja perinteisen suunnittelun ennakoinnin välillä. Ketterässä kehityksessä liian tarkkaa etukäteissuunnittelua karsastetaan. Arkkitehtuurisuunnittelu saatetaan nähdä asiana menneisyydestä, johon ei tarvi panostaa ja joka rakentuu muun toiminnan yhteydessä iteraatioiden mukana refaktorointia hyödyntäen. Toisaalta perinteisen suunnitteluvetoisen ohjelmistokehityksen kannattajat ovat saattaneet nähdä ketterät menetelmät hieman amatöörimäisenä touhuna, joka soveltuu hyvin vain tietynlaisiin, tyypillisesti kooltaan pieniin projekteihin. Artikkelin ja esimerkiksi saman aihepiirin kirjan Agile Software Architecture (Babar et al, 2013) kantavana teemana on tälläisen vastakkainasettelun häivyttäminen - ketteryys ja arkkitehtuuri voivat elää yhteiseloa olla jopa toisiaan tukevia asioita.

Oikealla tavalla suunniteltu arkkitehtuuri voi olla hyvä työkalu parantamaan ohjelmiston laatua sekä vähentämään kehitykseen käytettyä aikaa ja kuluja, kuten myös ketterät menetelmät voidaan nähdä laatua, tuottavuutta, kannattavuutta ja ennen kaikkea sovelluskehittäjien tyytyväisyyttä lisäävänä asiana.

## Kuinka arkkitehtuurisuunnittelua sovelletaan ketterässä ohjelmistokehityksessä

Yang et al. tutkimus A systematic mapping study on the combination of software architecture and agile development (2016) listaa 43 arkkitehtuurisuunnittelun lähestymistapaa sekä niihin liittyviä tutkimuksia. Listattuna ovat muun moassa iteratiivinen lähestymistapa sekä nollaiteraatio.

Iteratiivinen arkkitehtuuri (Emergent Architecture) sulauttaa arkkitehtuurisuunnittelun osaksi ketterän tuotannon iteraatoita. Arkkitehtuurisuunnittelua tehdään vain tarpeellinen määrä kyseisen iteraation tavoitteiden, eli käytännössä uusien käyttäjätoiminnallisuuksien toteuttamiseksi. Tässä mallissa arkkitehtuuri rakentuu refaktoroinnin kautta: sitä ei olla määritelty etukäteen vaan se kehittyy koodin mukana. 

Abrahamsson et al. artikkelissa todetaan, että arkkitehtuurin suunnittelu tulisi tehdä mahdollisimman aikaisin, sillä se kattaa merkittäviä päätöksiä järjestelmän rakenteesta ja käyttäytymisestä - näitä päätöksiä on vaikea kumota tai muuttaa myöhemmissä vaiheissa projektia.

Nollaiteraatiossa (Iteration Zero) on tarkoitus siirtää osa arkkitehtuurisuunnittelua tapahtuvaksi ennen varsinaista tuotantovaihetta olevaan iteraatioon sekä parantaa arkkitehtuuria tulevissa iteraatioissa. Tässä vaiheessa voidaan tehdä ns. walking skeleton, eli eräänlainen prototyyppi arkkitehtuurista, jonka tarkoitus on rakentua järjestelmän kasvaessa. Esimerkiksi Scrumiin on ollut ennen dokumentoituna ns. pregame-vaihe, jossa korkean tason arkkitehtuuri on määritelty. Tämä on kuitenkin poistettu myöhemmistä Scrumin kuvauksista. 

Ketterässä kehityksessä muutoksen pitäisikin olla ns. tavoiteltavissa oleva asia, joten etukäteen tehtävää arkkitehtuurisuunnittelua ei pitäisi periaatteessa esiintyä. 

Babar et al. (2013) kirjassa viitatun tutkimuksen mukaan Scrum-ohjelmistokehityksessä kuitenkin yleisesti hyödynnetään nollasprinttejä, BDUF-henkistä suunnittelua ja erillisten arkkitehtuuritiimien käyttöä. Abrahamsson et al. artikkelissa (2010) puhutaan Davide Falessin tutkimuksista, jossa ketterää hyödyntävät ohjelmistokehittäjät pitävät arkkitehtuuria merkityksellisenä apuvälineenä, joka muun muassa helpottaa kommunikointia ja suunnitteluvaihtoehtojen arviointia.

Ketterän manifestin mukaan parhaat arkkitehtuurit syntyvät itsenäisten kehitystiimin sisällä. Tämän voi nähdä lisäävän arkkitehtuuriin sitoutumista ja vähentävän dokumentaatioita. Toisaalta varsinkin suuremmissa organisaatioissa tämä ideaali ei välttämättä voi olla mahdollinen - arkkitehtuurilliset päätökset voi esimerkiksi tulla tiimin ulkopuolelta. Tällöin dokumentaation tärkeys korostuu.

Se, miten arkkitehtuuri ja ketterä ohjelmistotuotanto yhdistetään, ei ole itsestäänselvyys. Tästä on onneksi tehty tutkimusta - hyviä lähteitä aihepiirin tutkimukseen vaikuttaisi olevan esimerkiksi lähteissä mainitut Yang et al. kartoitustutkimus ja Babar et al. aiheesta koottu kirja.

# Lähteet

[Abrahamsson, P., Babar, M. A., & Kruchten, P. (2010). Agility and architecture: Can they coexist?. IEEE Software, 27(2), 16-22.](https://ieeexplore-ieee-org.libproxy.helsinki.fi/iel5/52/5420782/05420791.pdf)

[Babar, M. A., Brown, A. W., & Mistrík, I. (Eds.). (2013). Agile Software Architecture: Aligning Agile Processes and Software Architectures. Newnes.](https://helsinki.primo.exlibrisgroup.com/permalink/358UOH_INST/qn0n39/cdi_skillsoft_books24x7_bks00056508
)

[Beck, K., Beedle, M., van Bennekum, A., Cockburn, A., Cunningham, W., Fowler, M., Grenning, J., Highsmith, J., Hunt, A., Jeffries, R., Kern, J., Marick, B., Martin, R. C., Mellor, S., Schwaber, K., Sutherland, J. & Thomas, D. (2001). Manifesto for Agile Software Development Manifesto for Agile Software Development.](https://agilemanifesto.org/)

[Jen, L. R., & Lee, Y. J. (2000). Working Group. IEEE recommended practice for architectural description of software-intensive systems. In IEEE Architecture.](https://ieeexplore.ieee.org/document/875998)

[Yang, C., Liang, P., & Avgeriou, P. (2016). A systematic mapping study on the combination of software architecture and agile development. Journal of Systems and Software, 111, 157-184.](https://scholar-google-fi.libproxy.helsinki.fi/scholar?output=instlink&q=info:35snL_XCX8kJ:scholar.google.com/&hl=en&as_sdt=0,5&scillfp=15201364974769262941&oi=lle)

