> [!NOTE]  
> The English translation for this exercise can be found in [this file](./readme.en.md).

# Kurssin lämmittelytehtävät

Tämä repositorio sisältää joukon Java-harjoituksia, jotka auttavat sinua kertaamaan Ohjelmointi 1 -opintojakson sisältöjä ja perehtymään jatkokurssin harjoitusten tekniseen toteutukseen. Tässä repositoriossa käsitellään kolmea pääaihetta:

1. Merkkijonot
2. Kokoelmat
3. Luokat ja oliot

Tästä tiedostosta löydät tehtävänannot sekä ohjeet ratkaisusi testaamiseksi. Tarkemmat ohjeet kunkin metodin ja luokan toiminnasta löydät tehtäväpohjan valmiista Java-luokista.

Tehtävän kaikille osille on kirjoitettu valmiit [JUnit](https://junit.org/)-yksikkötestit, jotka sijaitsevat hakemistossa [src/test/java/](./src/test/java/). Voit suorittaa testit joko koodieditorisi testaustyökalulla ([VS Code](https://code.visualstudio.com/docs/java/java-testing), [Eclipse](https://www.vogella.com/tutorials/JUnitEclipse/article.html)) tai [Gradle-automaatiotyökalulla](https://docs.gradle.org/current/userguide/java_testing.html). Sinun ei tarvitse perehtyä testien tekniseen toteutukseen. Tässä vaiheessa riittää, että suoritat testit ja tutustut niiden mahdollisesti tuottamiin virheilmoituksiin.

Huomaa, että et saa muuttaa luokkien ja metodien nimiä etkä parametrien etkä paluuarvojen tyyppejä. Tällaiset muutokset aiheuttavat käännösvirheitä testeihin. Mikäli tulet muuttaneeksi tiedostoa ja haluat peruuttaa tekemäsi muutokset, voit tehdä sen `git restore`-komennolla:

```sh
git restore muutetun_tiedoston_polku
```


## Tehtävän aloittaminen

Forkkaa ensin tämä repositorio omaan GitHub-repositorioosi GitHubin **Fork**-painikkeella. Harjoitus tehdään omassa forkissasi, joten kloonaa vasta sitten oma forkkisi omalle koneellesi (osoitteessa on oma GitHub-käyttäjätunnuksesi):

```sh
git clone https://github.com/<oma-github-tunnuksesi>/<repositorion-nimi>.git
```

Kloonattuasi projektin omalle koneellesi, avaa se koodieditorissasi.


## Vastausten lähettäminen

Tämän tehtävän ratkaisuja ei arvioi mikään GitHub Actions -tehtävävirta (YAML-workflow), eikä `git push` käynnistä arviointia. Arvioinnin tekee kurssijärjestelmä: lähetä ratkaisusi tehtävän sivulla kurssijärjestelmässä, jolloin koodisi käännetään ja sille ajetaan tehtävän JUnit-testit.

Pushaa lopuksi kaikki julkiseen GitHub-repositorioosi ja paina tehtävän sivulla **Lähetä tarkistettavaksi** -nappia. Kurssijärjestelmän botti käy silloin hakemassa koodisi repositoriostasi ja tarkistaa sen samoilla testeillä.

💡 *Voit lähettää ratkaisusi niin monta kertaa kuin on tarpeen luvun määräaikaan asti. Voimaan jää paras saamasi tulos.*


### Osa 1: merkkijonot *(kertaus, 30 %)*

Java-luokassa [StringBasics](./src/main/java/part01/StringBasics.java) on metodeja, joista osa on virheellisiä ja osa toteuttamatta. Tehtävän ensimmäisessä osassa sinun tulee korjata ja täydentää nämä metodit. Tarkemmat selostukset kunkin metodin oikeasta toiminnasta löydät kunkin metodin kommenteista. Älä valmiiden metodien nimiä, parametreja tai paluuarvojen tyyppejä. Muutokset saattavat aiheuttaa ongelmia tehtävän automaattisen testauksen kanssa.

Voit kirjoittaa metodien testaamiseksi oman `main`-metodin tai hyödyntää luokan testaamiseksi toteutettuja [JUnit](https://junit.org/)-testejä, jotka löydät luokasta [StringBasicsTest](./src/test/java/part01/StringBasicsTest.java).

Voit suorittaa testit joko koodieditorisi testaustyökalulla ([VS Code](https://code.visualstudio.com/docs/java/java-testing), [Eclipse](https://www.vogella.com/tutorials/JUnitEclipse/article.html)) tai [Gradle-automaatiotyökalulla](https://docs.gradle.org/current/userguide/java_testing.html):

```
./gradlew test --tests StringBasicsTest        # unix
.\gradlew.bat test --tests StringBasicsTest    # windows
```

💡 *Jos testit eivät mene läpi, kokeile suorittaa komento uudestaan siten, että lisäät loppuun argumentin `--info`. Näin saat tarkemman tiedon siitä, mikä testissä meni pieleen. Vaihtoehtoisesti voit suorittaa testit koodieditorin testaustyökalulla ([VS Code](https://code.visualstudio.com/docs/java/java-testing), [Eclipse](https://www.vogella.com/tutorials/JUnitEclipse/article.html)), joka tyypillisesti näyttää virheet selkeästi.*

💡 *Sinun ei tarvitse perehtyä varsinaisen testin tekniseen toteutukseen. Tässä vaiheessa riittää, että suoritat testit ja tutustut niiden mahdollisesti tuottamiin virheilmoituksiin.*


### Osa 2: kokoelmat *(kertaus, 30 %)*

Tehtävän toisessa osassa sinun tulee toteuttaa [CollectionsBasics](./src/main/java/part02/CollectionsBasics.java)-luokassa olevat metodit. Tarkemmat selostukset kunkin metodin oikeasta toiminnasta löydät kunkin metodin kommenteista.

Voit kirjoittaa metodien testaamiseksi oman `main`-metodin tai hyödyntää luokan testaamiseksi toteutettuja [JUnit](https://junit.org/)-testejä, jotka löydät luokasta [CollectionsBasicsTest](./src/test/java/part02/CollectionsBasicsTest.java). Voit jälleen suorittaa testit oman koodieditorisi testaustyökalulla tai Gradle-automaatiotyökalulla:

```
./gradlew test --tests CollectionsBasicsTest        # unix
.\gradlew.bat test --tests CollectionsBasicsTest    # windows
```

🚀 *Tulet todennäköisesti oppimaan kurssin edetessä aivan uusia tapoja näiden metodien toteuttamiseksi. Voit palata näihin metodeihin myöhemmin ja pohtia, miten toteuttaisit ne esimerkiksi Streamien avulla.*


### Osa 3: luokat ja oliot *(kertaus, 20 + 20 %)*

Tehtävän kolmannessa osassa sinun tulee ensin täydentää kahta Java-luokkaa:

* [Person](./src/main/java/part03/Person.java) on varsin yksinkertainen Java-luokka, joka mallintaa henkilöitä, joilla on nimi ja ikä. Luokan toteutus on kesken ja sinun tulee täydentää se toimivaksi luokan ja metodien kommenttien mukaisesti.
* [ObjectExercise](./src/main/java/part03/ObjectExercise.java)-luokka puolestaan sisältää yhden metodin, jossa sinun on tarkoitus käsitellä `Person`-olioita ja yhdistellä henkilöiden nimet yhdeksi merkkijonoksi. Tarkemmat säännöt nimien yhdistämiseksi löydät metodin kommenteista.

Oman toteutuksen testaaminen tapahtuu edellisistä osista tuttuun tapaan oman `main`-metodin tai valmiiden JUnit-yksikkötestien avulla ([PersonTest.java](./src/test/java/part03/PersonTest.java), [ObjectExerciseTest.java](./src/test/java/part03/ObjectExerciseTest.java)). Mikäli käytät Gradle-työkalua, voit suorittaa testit komennolla:

```
# unix
./gradlew test --tests PersonTest
./gradlew test --tests ObjectExerciseTest

# windows
.\gradlew.bat test --tests PersonTest
.\gradlew.bat test --tests ObjectExerciseTest
```


## Lisenssi ja tekijät

Tämän tehtävän on kehittänyt Teemu Havulinna ja se on lisensoitu [Creative Commons BY-NC-SA -lisenssillä](https://creativecommons.org/licenses/by-nc-sa/4.0/).

Tehtävänannon, lähdekoodien ja testien toteutuksessa on hyödynnetty ChatGPT 3.5 -kielimallia sekä GitHub copilot -tekoälyavustinta.

## Ratkaisun tallentaminen

Tee tästä tehtäväpohjasta oma kopio (fork tai kopio) ja tallenna ratkaisusi myös **yksityiseen (private) GitHub-repositorioon omalla GitHub-tililläsi**. Älä julkaise ratkaisuasi julkisessa repositoriossa.

Palauta ratkaisusi opettajan ilmoittamaan palautusjärjestelmään.
