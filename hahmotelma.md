*(tämä on vasta hahmotelma joka päivittyy, tarkentuu ja kasvaa vielä)*

# Ohjelmiston arkkitehtuurisuunnittelu ketterissä menetelmissä

Ohjelmiston arkkitehtuuri on IEEE:n standardin mukaan ohjelmiston perusorganisaatio, joka sisältää järjestelmän osat, niiden keskenäiset suhteet ja suhteet ympäristöön. Arkkitehtuuri ohjaa järjestelmän suunnittelua ja evoluutiota. 

Rational Unified Process määrittelee ohjelmistoarkkitehtuurin joukkona perustavanlaatuisia päätöksiä koskien järjestelmän organisaatiota, rakenteellisia elementtejä, rajapintoja, elementtien käyttäytymistä toistensa kanssa, elementtien yhdistämistä alijärjestelmiksi, alijärjestelmien arkkitehtuurillista tyyliä ja niin edelleen. RUP:in mukaan arkkitehtuurissa ei olla kiinnostuneita pelkästään rakenteesta ja toiminnasta, mutta myös käytöstä, toiminnallisuudesta, suorituskyvystä, joustavuudesta, uudelleenkäytettävyydestä ja ymmärrettävyydestä. Arkkitehtuurissa pitää ottaa huomioon myös taloudelliset ja teknologisista rajoitteet.

Nykyään suosioon nousseita ketteriä menetelmiä, kuten Scrumia ja Extreme programmingia, yhdistää iteratiivinen ja inkrementaalinen elinkaari, pienissä erissä tapahtuvat julkaisut, yhtenäinen tiimi sekä ominaisuus- tai tuotebacklogiin perustuva julkaisusuunnitelma. Olennaista on myös pyrkiminen prosessin yksinkertaisuuteen ja sopeutuminen vaatimusten muutoksiin.

Perinteisessä ohjelmistotuotannossa, kuten vesiputousmallissa, ohjelmistoon liittyvä suunnittelu tapahtuu tyypillisesti ennen varsinaista sovelluksen toteutusvaihetta.
Tämä Big Design Up-Front (BDUF) -käytäntö sisältää myös ohjelmiston arkkitehtuurin suunnittelun.

Ketterät menetelmät ei sen sijaan usein kerro juurikaan mitään arkkitehtuurista. Esimerkiksi Scrumiin ei ole määritelty, kuinka arkkitehtuurisuunnittelu tulisi toteuttaa. Extreme programmingissa arkkitehtuurin rakentumista määrittelee ainoastaan järjestelmämetafora (system metaphor).

Ketterän ohjelmistokehityksen periaatteet ovat jokseenkin epäsuhdassa arkkitehtuuriperustaisen ohjelmistosuunnittelun kanssa. Ketterän manifestin mukaan esimerkiksi muutokseen reagoimista pidetään tärkeämpänä kuin tarkkojen suunnitelmien noudattamista. Halutaan minimoida kaikki turha työ, jota saattaa syntyä, jos arkkitehtuuriin tullaan tekemään muutoksia myöhemmässä vaiheessa. Asiakkaalle arvoa tuottavien ohjelmiston nopea tuottaminen nähdään tärkempänä asiana kuin tarkka suunnittelu ja dokumentaatio. Ketterässä kehityksessä ihanteena on, että päätökset pyritään tekemään mahdollisimman myöhäisessä vaiheessa.

Abrahamsson et al. artikkelissa Agility and architecture: Can they coexist? (2010) mukaan suurin arkkitehtuurin muodostamisen vastakkainasettelu näyttää olevan kettärelle kehitykselle ominaisen sopeutumisen ja perinteisen suunnittelulle ominaisen ennakoinnin välillä. Ketterän kannattajat saattavat pitävää arkkitehtuuria asiana menneisyydestä, johon ei pidä panostaa ja joka rakentuu muun toiminnan yhteydessä iteraatio iteraatiolta refaktorointia hyödyntäen. Toisaalta perinteisen vesiputousmallisen ohjelmistokehityksen kannattajat ovat saattaneet nähdä ketterät menetelmät hieman amatöörimäisenä touhuna, joka soveltuu hyvin vain tiettyihin sovellutuksiin. Artikkelin ja esimerkiksi saman aihepiirin kirjan Agile Software Architecture (Babar et al, 2013) kantavana teemana on tälläisen vastakkainasettelun häivyttäminen - ketteryys ja arkkitehtuuri voivat elää yhteiseloa ja jopa tukea toisiansa erilaisissa konteksteissa.

Oikealla tavalla suunniteltu arkkitehtuuri voi olla hyvä työkalu vähentämään kehitykseen käytettyä aikaa ja kuluja sekä parantamaan ohjelmiston laatua, kuten myös ketterät menetelmät nähdään laatua, tuottavuutta, kannattavuutta ja ennen kaikkea sovelluskehittäjien tyytyväisyyttä lisäävänä asiana.

## Kuinka arkkitehtuurisuunnittelua sovelletaan ketterässä ohjelmistokehityksessä

Yang et al. tutkimus A systematic mapping study on the combination of software architecture and agile development (2016) listaa 43 arkkitehtuurisuunnittelun lähestymistapaa sekä niihin liittyviä tutkimuksia. Listattuna ovat muun moassa iteratiivinen lähestymistapa sekä nollaiteraatio.

Iteratiivinen arkkitehtuuri (Emergent Architecture) sulauttaa arkkitehtuurisuunnittelun osaksi ketterän tuotannon iteraatoita ja arkkitehtuurisuunnittelua tehdään vain tarpeellinen määrä kyseisen iteraation tavoitteiden, eli käytännössä uusien käyttäjätoiminnallisuuksien toteuttamiseksi. Tässä mallissa arkkitehtuuri rakentuu refaktoroinnin kautta eli se kehittyy koodin mukana eikä sitä olla määritelty etukäteen. 

Abrahamsson et al. artikkelissa todetaan, että suunnittelu tulisi tehdä mahdollisimman aikaisin, sillä se kattaa merkittäviä päätöksiä järjestelmän rakenteesta ja käyttäytymisestä. Näitä
päätöksiä on vaikea kumota tai muuttaa myöhemmässä vaiheessa. Esimerkiksi nollaiteraatiossa (Iteration Zero) on tarkoitus siirtää osa arkkitehtuurisuunnittelua tapahtuvaksi ennen varsinaista tuotantovaihetta olevaan iteraatioon sekä parantaa arkkitehtuuria tulevissa iteraatioissa. Tässä vaiheessa voidaan tehdä ns. walking skeleton, eli eräänlainen prototyyppi arkkitehtuurista, jonka tarkoitus on rakentua järjestelmän kasvaessa.

Scrumiin on ollut ennen dokumentoituna ns. pregame-vaihe, jossa korkean tason arkkitehtuuri on määritelty, mutta se on poistettu myöhemmistä Scrumin kuvauksesta. Ketterässä kehityksessä muutoksen pitäisikin olla jopa tavoiteltavissa oleva asia, joten etukäteen tehtävää arkkitehtuurin suunnittelua ei pitäisi periaatteessa esiintyä. Babar et al. (2013) Scrumia käsittelävän kappaleen mukaan käytännössä Scrum-ohjelmistokehityksessä kuitenkin hyödynnetään nollasprinttejä ja jopa BDUF-henkistä suunnittelua sekä erillisten arkkitehtuuritiimien käyttöä.

Ketterän manifestin mukaan parhaat arkkitehtuurit syntyvät itsenäisten kehitystiimien toimesta. Tämä lisää arkkitehtuuriin sitoutumista ja helpottaa dokumentaatioita ...

# Lähteet

Artikkeli:
[Abrahamsson, P., Babar, M. A., & Kruchten, P. (2010). Agility and architecture: Can they coexist?. IEEE Software, 27(2), 16-22.](https://ieeexplore-ieee-org.libproxy.helsinki.fi/iel5/52/5420782/05420791.pdf)

Kirja:
[Babar, M. A., Brown, A. W., & Mistrík, I. (Eds.). (2013). Agile Software Architecture: Aligning Agile Processes and Software Architectures. Newnes.](https://helsinki.primo.exlibrisgroup.com/permalink/358UOH_INST/qn0n39/cdi_skillsoft_books24x7_bks00056508
)

Agile manifesto:
[Beck, K., Beedle, M., van Bennekum, A., Cockburn, A., Cunningham, W., Fowler, M., Grenning, J., Highsmith, J., Hunt, A., Jeffries, R., Kern, J., Marick, B., Martin, R. C., Mellor, S., Schwaber, K., Sutherland, J. & Thomas, D. (2001). Manifesto for Agile Software Development Manifesto for Agile Software Development.](https://agilemanifesto.org/)

IEEE-standardi:
[Jen, L. R., & Lee, Y. J. (2000). Working Group. IEEE recommended practice for architectural description of software-intensive systems. In IEEE Architecture.](https://ieeexplore.ieee.org/document/875998)

Mapping-study:
[Yang, C., Liang, P., & Avgeriou, P. (2016). A systematic mapping study on the combination of software architecture and agile development. Journal of Systems and Software, 111, 157-184.](https://scholar-google-fi.libproxy.helsinki.fi/scholar?output=instlink&q=info:35snL_XCX8kJ:scholar.google.com/&hl=en&as_sdt=0,5&scillfp=15201364974769262941&oi=lle)

