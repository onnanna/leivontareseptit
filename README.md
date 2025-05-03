# leivontareseptit

Sovelluksessa käyttäjät pääsevät jakamaan suosikkireseptejä muiden käyttäjien kanssa. Leivontareseptejä pääsee kommentoimaan, kertoa miten itsellä sujui reseptin leipominen tai pyytää vinkkejä leivonnassa onnistumiseen.

## Sovelluksen toiminnot

* Käyttäjä pystyy luomaan tunnuksen ja kirjautumaan sisään sovellukseen
* Käyttäjä pystyy lisäämään, muokkaamaan ja poistamaan leivontareseptejä
* Käyttäjä pystyy lisäämään kuvia resepteihin
* Käyttäjä näkee sovellukseen lisätyt leivontareseptejä, itse lisäämänsä että muiden käyttäjien lisäämät ohjeet
* Käyttäjä pystyy etsimään reseptejä hakusanalla
* Sovelluksessa on käyttäjäsivut, jotka näyttävät käyttäjästä tilastoja ja käyttäjän lisäämät leivontaohjeet
* Käyttäjä pystyy valitsemaan leivontaohjeelle yhden tai useamman luokittelun (esim. makea, suolainen, vegaaninen, laktoositon, vaikeustaso)
* Käyttäjä pystyy kommentoimaan leivontaohjeita

## Sovelluksen asennus
Asenna `flask`-kirjasto:
```
$ pip install flask
```

Luo tietokannan taulut ja lisää alkutiedot:
```
$ sqlite3 database.db < schema.sql
$ sqlite3 database.db < init.sql
```

Sovelluksen käynnistäminen:
```
$ flask run
```

### Välipalaututukset:
Tilanne välipalautus 2 kohdalla:
- Käyttäjä pystyy luomaan tunnuksen ja kirjautumaan sisään
- Käyttäjä pystyy lisäämään, muokkaamaan ja poistamaan omia reseptejään
- Käyttäjä näkee lisätyt ohjeet, omansa ja muiden lisäämät
- Ohjeita pystyy etsimään hakusanalla

Tilanne välipalautus 3 kohdalla:
- Annetun tekstin muotoa tarkistetaan
- Käyttäjäsivuilta näkee käyttäjän lisäämät reseptit
- Reseptille voi valita luokan, luokkavaihtoehdot ovat vielä vähän heikot (pitää vielä kokeilla lisätä jotenkin että luokkia pystyy valita useamman samoista vaihtoehdoista)
- Toisten käyttäjien reseptien kommentointi onnistuu melkein
