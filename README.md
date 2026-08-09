# Rautakausiretki
Geolibre-karttaretki, demo 1

Staattinen GeoLibre karttatarina  valikoiduista Satakunnan viikinkiajan arkeologisista kohteista. Teknisesti tyhdistetty karttasiirtymät, kohdepisteet, kuvamateriaalin ja lyhyet tekstikortit selaimessa toimivaksi karttatarinaksi. 

Tekniikka: GeoLibre StoryMaps, JSON/GeoJSON, GitHub Pages, ChatGPT Sol5.6 Korkea
Karttaretki Satakunnan viikinkiajan arkeologisiin kohteisiin. GeoLibre StoryMaps -toteutus yhdistää kartan, kohdekuvat ja lyhyet arkeologiset tekstikortit yhdeksi virtuaaliseksi matkaksi.

Tekijä & toimitus: Nina Mäki-Kihniä.
Lähteet: VARK, KYPPi, Finna sekä kohdekohtaisesti mainitut arkeologiset julkaisut.

Sivusto on tekninen harjoitus. Toteutus sisältää AI-avusteisia/generoituja työvaiheita. Sisällössä, tulkinnoissa tai teknisessä toteutuksessa voi olla virheitä.

# Kuvien lähteet ja käyttöoikeudet

Verkkosivulla käytetyt kuvat on pienennetty ja optimoitu verkkokäyttöön. Alkuperäisen kuvan sisältöä ei ole tarkoituksellisesti muutettu; GeoLibreä varten joihinkin kuviin on lisätty kehystilaa kuvasuhteen sovittamiseksi.

## 01\_eura\_luistari.jpg

* Kuvaaja: Leena Koivisto
* Vuosi: 2009
* Organisaatio: Satakunnan Museo
* Lisenssi: CC BY 4.0
* Lähde: https://www.finna.fi/Record/museovirasto.6F835FF3661121A7538996C48C5279EF?sid=5451478102

## 02\_eura\_emanta\_geolibre.jpg

* Kuvaaja: Matti Bergström
* Vuosi: ei ilmoitettu lähdetietueessa
* Organisaatio: Museovirasto
* Lisenssi: CC BY 4.0
* Lähde: https://www.finna.fi/Record/musketti.M012:AKD7157:1

## 03\_kauttua\_linnavuori.jpg

* Kuvaaja: Leena Koivisto
* Vuosi: 2011
* Organisaatio: Satakunnan Museo
* Lisenssi: CC BY 4.0
* Lähde: https://satakunnanmuseo.finna.fi/Record/satakunnanmuseo.44EF6E1E-75FE-4DA5-BB43-541572C337A2?sid=5451393709

## 04\_tupamaki\_rautakuona.jpg

* Kuvaaja: Teija Tiitinen
* Vuosi: 2021
* Organisaatio: Museovirasto
* Lisenssi: CC BY 4.0
* Lähde: https://finna.fi/Record/museovirasto.013353e5-d960-40e3-8a7d-99fe91eb5cb2?sid=5451487213

## 05\_koylio\_lallin\_kalmisto.jpg

* Tekijä: A. Hackman
* Vuosi: 1925
* Organisaatio: Museovirasto / Kulttuuriympäristön palveluikkuna (KYPPi)
* Lähde: https://www.kyppi.fi/to.aspx?id=129.130352

## 06\_tuhkanummi.jpg

* Kuvaaja: Teemu Väisänen
* Vuosi: 2019
* Organisaatio: Satakunnan Museo
* Lisenssi: CC BY 4.0
* Lähde: https://www.finna.fi/Record/satakunnanmuseo.7D6C0753-9E1E-41AE-BB9A-40D597753CFE?sid=5451490915

## 07\_villionsuvanto\_liesi.jpg

* Kuvaaja: Leena Koivisto
* Vuosi: 2019
* Organisaatio: Satakunnan Museo
* Lisenssi: CC BY 4.0
* Lähde: https://www.finna.fi/Record/satakunnanmuseo.35BBE115-BF9A-49D9-BF26-D7D9114DE840?sid=5451492481

## 08\_peravainionmaki.jpg

* Kuvaaja: Teemu Väisänen
* Vuosi: 2019
* Organisaatio: Satakunnan Museo
* Lisenssi: CC BY 4.0
* Lähde: https://www.finna.fi/Record/satakunnanmuseo.1B849E63-5698-4CFD-85CB-AD848F3457ED?sid=5451494515

## 10\_hankkasmaki\_kupurasolki.jpg

* Kuvaaja: Teemu Väisänen
* Vuosi: 2024
* Organisaatio: Satakunnan Museo
* Lisenssi: CC BY 4.0
* Lähde: https://www.finna.fi/Record/satakunnanmuseo.087e7fbf-db2b-4df9-b53f-230ef99fc9e0?sid=5451496576

## 11\_lopetus\_hankkasmaki\_maisema\_geolibre.jpg

* Kuvaaja: Teemu Väisänen
* Vuosi: 2025
* Julkaisu / organisaatio: Muinaistutkija 3/2025 / Suomen arkeologinen seura
* Lähde: https://doi.org/10.61258/mt.173127

# Tekniset muistiinpanot GeoLibrestä

GeoLibre ei näyttänyt kaikkia kuvia vakaasti.
→ Kuvat siirrettiin Finna/KYPPi-suoralinkeistä omaan GitHub Pages images/ -hakemistoon.
Base64-kuvat tekivät .geolibre.json-tiedostosta valtavan ja hankalan muokata.
→ Kuvakentät vaihdettiin tavallisiksi HTTPS-kuvalinkeiksi.
Pystysuuntaiset kuvat rajautuivat GeoLibren leveissä kuvalohkoissa.
→ Tehtiin erillisiä GeoLibre/web-versioita, joissa koko kuva mahtuu leveään kehykseen ilman varsinaisen kuvasisällön leikkaamista.
Pitkät otsikot katkeavat kapealla näytöllä.
→ GeoLibre-versiossa otsikkopalkki pidetään lyhyenä ja pidempi tarinallinen otsikko voidaan sijoittaa tekstin alkuun.
JSON rikkoutui helposti käsin muokattaessa.
→ Muutokset rajattiin pääasiassa yksittäisiin image-kenttiin; Markdown-linkkejä ei käytetä JSONissa, vaan paljaita URL-osoitteita.
Sama tieto esiintyi useissa JSON/GeoJSON-varatiedostoissa.
→ Yksi .geolibre.json toimii master-projektina; muut tiedostot ovat lähinnä varmuus- ja työaineistoa.
Kuvaoikeudet vaihtelevat lähteittäin.
→ Kuville koottiin erillinen CREDITS.md, jossa ovat kuvaaja, vuosi, organisaatio, lähde ja lisenssi/oikeustilanne.
GeoLibren Present-näkymällä on typografisia ja asetteluun liittyviä rajoituksia.
→ GeoLibreä käytetään kartan ja tarinasiirtymien rakentamiseen; lopullinen julkaisu voidaan viimeistellä GitHub Pagesiin vietävässä HTML-versiossa.
