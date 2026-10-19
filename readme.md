> [!NOTE]
> The English translation for this exercise can be found in [this file](./readme.en.md).

# Kurssin lämmittelytehtävät

Tämä repositorio sisältää Java-harjoituksia, joiden avulla kertaat Ohjelmointi 1 -opintojakson sisältöjä ja tutustut jatkokurssin harjoitusten tekniseen toteutukseen. Harjoitusten aiheet ovat merkkijonot, kokoelmat sekä luokat ja oliot. Tarkemmat ohjeet kunkin metodin ja luokan toiminnasta löydät tehtäväpohjan Java-luokkien kommenteista.

## Tehtävän aloittaminen

Forkkaa ensin tämä repositorio omaan GitHub-repositorioosi GitHubin **Fork**-painikkeella ja kloonaa vasta sitten oma forkkisi koneellesi:

```sh
git clone https://github.com/<oma-github-tunnuksesi>/2-warming-up.git
```

Avaa kloonattu projekti koodieditorissasi.

## Testaaminen

Tehtävän osille on valmiit [JUnit](https://junit.org/)-yksikkötestit hakemistossa [src/test/java](./src/test/java/). Kunkin osan kohdalla kerrotaan, millä testiluokalla se arvioidaan. Voit ajaa testit koodieditorisi testaustyökalulla ([VS Code](https://code.visualstudio.com/docs/java/java-testing), [Eclipse](https://www.vogella.com/tutorials/JUnitEclipse/article.html)) tai [Gradlella](https://docs.gradle.org/current/userguide/java_testing.html), esimerkiksi:

```
./gradlew test --tests StringBasicsTest        # unix
.\gradlew.bat test --tests StringBasicsTest    # windows
```

Lisää komennon loppuun `--info`, jos haluat tarkemmat tiedot epäonnistuneista testeistä. Testien tekniseen toteutukseen ei tarvitse perehtyä, ja voit kokeilla ratkaisuasi myös omalla `main`-metodilla. Saat kirjoittaa omia testejä lisää, mutta älä muuta tai poista valmiita testejä.

Älä muuta valmiiden luokkien, metodien ja konstruktorien nimiä, parametreja tai paluuarvojen tyyppejä, sillä silloin testit eivät käänny. Saat tiedoston alkuperäisen version takaisin komennolla `git restore <tiedoston polku>` tai kurssijärjestelmän **Palauta lähtökoodi** -toiminnolla.

## Palauttaminen ja pisteet

Jokaisella tehtävän osalla on kurssijärjestelmässä (https://jtjuslin.kapsi.fi/java) oma sivunsa, jonka koodikentissä on osan koodipohja. Kopioi ratkaisusi koodikenttiin tai kirjoita se suoraan niihin. **Testaa ilman palautusta** ajaa osan testit tallentamatta pisteitä, ja **Lähetä** palauttaa ratkaisun. Jokainen testiluokka hyväksytään vain, jos sen kaikki testit menevät läpi, ja pisteet jaetaan hyväksyttyjen testiluokkien mukaan.

**Pisteet kahdessa vaiheessa**

1. Kun ratkaisusi menee läpi kurssijärjestelmässä, saat osasta **puolet pisteistä**.
2. Pushaa lopuksi kaikki julkiseen GitHub-repositorioosi. Paina tämän jälkeen osan sivulla **Lähetä tarkistettavaksi** -nappia. Kun testit menevät läpi, saat osasta **täydet pisteet**. Repositorio saa jäädä julkiseksi.

GitHubissa ei ole arvioivaa YAML-tehtävävirtaa (GitHub Actions -workflowta), eikä `git push` käynnistä arviointia. Kun painat **Lähetä tarkistettavaksi**, kurssijärjestelmän botti hakee koodisi repositoriostasi ja tarkistaa sen samoilla testeillä. Molemmat vaiheet pitää tehdä ennen luvun määräaikaa. Voit lähettää ratkaisusi niin monta kertaa kuin tarvitset, ja voimaan jää paras tulos.


## Osa 1: merkkijonot *(kertaus, 30 %)*

Java-luokassa [StringBasics](./src/main/java/part01/StringBasics.java) on metodeja, joista osa on virheellisiä ja osa toteuttamatta. Korjaa ja täydennä metodit niiden kommenttien mukaisesti. `centerMultiLine` on vapaaehtoinen lisätehtävä: jos se palauttaa `null`, sen testi ohitetaan.

Arvioinnissa ajetaan testiluokka [StringBasicsTest](./src/test/java/part01/StringBasicsTest.java).

💡 *Epäonnistuneen testin viesti kertoo, mitä odotettiin. Esimerkiksi `expected: <He> but was: <Hello>` tarkoittaa, että testi odotti arvoa He, mutta metodisi palautti Hello.*


## Osa 2: kokoelmat *(kertaus, 30 %)*

Toteuta [CollectionsBasics](./src/main/java/part02/CollectionsBasics.java)-luokan metodit niiden kommenttien mukaisesti. Metodit käsittelevät listoja: suurin arvo, summa, kertominen, lukuväli, merkkijonojen yhdistäminen, pituudet ja osajonon esiintymät.

Arvioinnissa ajetaan testiluokka [CollectionsBasicsTest](./src/test/java/part02/CollectionsBasicsTest.java).

🚀 *Opit kurssin aikana uusia tapoja toteuttaa nämä metodit. Voit palata niihin myöhemmin ja pohtia, miten toteuttaisit ne esimerkiksi streamien avulla.*


## Osa 3: luokat ja oliot *(kertaus, 20 % + 20 %)*

Täydennä kaksi Java-luokkaa:

* [Person](./src/main/java/part03/Person.java) mallintaa henkilöä, jolla on nimi ja ikä. Toteuta sen oliomuuttujat, konstruktori ja getterit luokan ja metodien kommenttien mukaisesti.
* [ObjectExercise](./src/main/java/part03/ObjectExercise.java)-luokan metodi käsittelee `Person`-olioiden listaa ja yhdistää henkilöiden nimet yhdeksi merkkijonoksi. Tarkemmat säännöt ovat metodin kommenteissa.

Arvioinnissa ajetaan testiluokat [PersonTest](./src/test/java/part03/PersonTest.java) (puolet pisteistä) ja [ObjectExerciseTest](./src/test/java/part03/ObjectExerciseTest.java) (puolet pisteistä).


## Lisenssi ja tekijät

Tämän tehtävän ovat kehittäneet Teemu Havulinna ja Jukka Juslin, ja se on lisensoitu [Creative Commons BY-NC-SA -lisenssillä](https://creativecommons.org/licenses/by-nc-sa/4.0/). Tehtävänannon, lähdekoodien ja testien toteutuksessa on hyödynnetty ChatGPT 3.5 -kielimallia sekä GitHub Copilot -tekoälyavustinta.
