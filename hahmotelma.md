*(tämä on vasta hahmotelma joka päivittyy ja kasvaa vielä)*

# Ohjelmiston arkkitehtuurisuunnittelu ketterissä menetelmissä

Ohjelmiston arkkitehtuuri on IEEE:n standardin Recommended practices for Architectural descriptions of Software intensive systems (2000) mukaan ohjelmiston perusorganisaatio, joka sisältää järjestelmän osat, niiden keskenäiset suhteet ja suhteet ympäristöön. Arkkitehtuuri ohjaa järjestelmän suunnittelua ja evoluutiota.

Perinteisessä ohjelmistotuotannossa, kuten vesiputousmallissa, ohjelmistoon liittyvä suunnittelu on tapahtunut tyypillisesti ennen varsinaista sovelluksen toteutusvaihetta.
Tämä Big Design Up-Front (BDUF) -käytäntö on ulottunut myös arkkitehtuurin suunnitteluun.

Nykyään suositun ketterän ohjelmistokehityksen arvot osin sotii etukäteen tehtävää arkkitehtuurisuunnittelua vastaan. Ketterän manifestin mukaan esimerkiksi muutokseen reagoimista pidetään tärkeämpänä kuin tarkkojen suunnitelmien noudattamista. Halutaan minimoida kaikki turha työ, jota saattaa syntyä, jos arkkitehtuuriin tullaan tekemään muutoksia myöhemmässä vaiheessa. Päätökset pyritään tekemään mahdollisimman myöhäisessä vaiheessa. Asiakkaalle arvoa tuottavien ohjelmiston nopea tuottaminen nähdään tärkempänä kuin tarkka suunnittelu ja dokumentaatio sijaan. 

On laajasti tiedostettu, että suunniteltu arkkitehtuuri voi olla hyvä työkalu vähentämään kehitykseen käytettyä aikaa ja kuluja sekä parantamaan ohjelmiston laatua (Babar, et al). Ketterän ohjelmistotuotannon prosessien luotettavuutta, tehokkuutta ja skaalautuvuutta kohtaan on oltu skeptisiä koska ne eivät anna tarpeeksi painoarvoa arkkitehtuuriin liittyville periaatteille ja käytännöille (Abrahamsson et al.).

Abrahamsson et. al artikkelissa todetaan, että arkkitehtuurisuunnittelu ja ketterä ohjelmistokehitys eivät ole toisiaan poissulkevia.

## Kuinka arkkitehtuurisuunnittelua sovelletaan ketterässä ohjelmistokehityksessä

Yang et al. tutkimus A systematic mapping study on the combination of software architecture and agile development (2016) listaa 43 arkkitehtuurisuunnittelun lähestymistapaa sekä niihin liittyviä tutkimuksia. Listattuna ovat mm. iteratiivinen lähestymistapa sekä nollaiteraatio.

Iteratiivinen arkkitehtuuri sulauttaa arkkitehtuurisuunnittelun osaksi ketterän tuotannon iteraatoita ja arkkitehtuurisuunnittelua tehdään vain tarpeellinen määrä kyseisen iteraation toiminnallisuuksien toteuttamiseksi (Yang et al.). Iteratiivinen arkkitehtuuri tunnetaan myös nimellä Emergent Architecture. Babar et al. mukaan tässä mallissa arkkitehtuuri rakentuu refaktoroinnin kautta eli se kehittyy koodin mukana eikä sitä olla määritelty etukäteen. 

Nollaiteraatiossa (Iteration Zero) on tarkoitus siirtää osa arkkitehtuurisuunnittelusta tapahtuvaksi ennen varsinaista tuotantovaihetta sekä paranatta arkkitehtuuria tulevissa iteraatioissa. Esimerkiksi muuten ketterän ja inkrementaalisen  ohjelmistosuunnittelukehyksen Scrum-viitekehyksessä on ollut käytössä ns. pregame-vaihe, jossa korkean tason arkkitehtuuri on määritelty, mutta se on poistettu myöhemmistä Scrumin kuvauksista (Scrum book).

Babar et al. kirjan Aligning Agile Processes and Software Architectures (2013) kappaleessa Architecting while using Scrum käsitellään arkkitehtuurisuunnittelua  Scrumin kontekstissa. Ketterässä kehityksessä muutoksen pitäisi olla jopa tavoiteltavissa oleva asia, joten etukäteen tehtävää arkkitehtuurin suunnittelua ei pitäisi periaatteessa edes esiintyä. Viitatun tutkimuksen mukaan käytännössä kuitenkin hyödynnetään BDUF-henkistä suunnittelua, nollasprinttejä ja erillisten arkkitehtuuritiimien käyttöä.



# Lähteet

[Abrahamsson, P., Babar, M. A., & Kruchten, P. (2010). Agility and architecture: Can they coexist?. IEEE Software, 27(2), 16-22.](https://ieeexplore-ieee-org.libproxy.helsinki.fi/iel5/52/5420782/05420791.pdf)

[Babar, M. A., Brown, A. W., & Mistrík, I. (Eds.). (2013). Agile Software Architecture: Aligning Agile Processes and Software Architectures. Newnes.](https://helsinki.primo.exlibrisgroup.com/permalink/358UOH_INST/qn0n39/cdi_skillsoft_books24x7_bks00056508
)

[Jen, L. R., & Lee, Y. J. (2000). Working Group. IEEE recommended practice for architectural description of software-intensive systems. In IEEE Architecture.](https://ieeexplore.ieee.org/document/875998)

[Yang, C., Liang, P., & Avgeriou, P. (2016). A systematic mapping study on the combination of software architecture and agile development. Journal of Systems and Software, 111, 157-184.](https://scholar-google-fi.libproxy.helsinki.fi/scholar?output=instlink&q=info:35snL_XCX8kJ:scholar.google.com/&hl=en&as_sdt=0,5&scillfp=15201364974769262941&oi=lle)

