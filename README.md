# Rautakausiretki
Geolibre-karttaretki, demo 1

Staattinen GeoLibre karttatarina  valikoiduista Satakunnan viikinkiajan arkeologisista kohteista. Teknisesti yhdistetty karttasiirtymät, kohdepisteet, kuvamateriaalin ja lyhyet tekstikortit ensisijaisesti desktop-selaimessa toimivaksi karttatarinaksi. 

Tekniikka: GeoLibre StoryMaps, JSON/GeoJSON, GitHub Pages, ChatGPT Sol5.6 Korkea
Karttaretki Satakunnan viikinkiajan arkeologisiin kohteisiin. GeoLibre StoryMaps -toteutus yhdistää kartan, kohdekuvat ja lyhyet arkeologiset tekstikortit yhdeksi virtuaaliseksi matkaksi.

Tekijä & toimitus: Nina Mäki-Kihniä.
Lähteet: VARK, KYPPi, Finna sekä kohdekohtaisesti mainitut arkeologiset julkaisut.

Sivusto on tekninen harjoitus. Toteutus sisältää AI-avusteisia/generoituja työvaiheita. Sisällössä, tulkinnoissa tai teknisessä toteutuksessa voi olla virheitä.

# Tekniset muistiinpanot GeoLibrestä


Sivusto julkaistaan GitHub Pagesissa. `index.html` sisältää GeoLibre-projektin JSON-muodossa ja välittää sen selaimessa GeoLibre-viewerille.

~~~
GitHub Pages / index.html
        │
        ├── tekstit
        ├── karttapisteet
        ├── zoomaukset ja karttasiirtymät
        ├── kuvalinkit
        └── StoryMap-rakenne
                 │
                 ▼
        web.geolibre.app
        näyttää projektin
~~~

Ulkoiset resurssit:

- `GitHub Pages / images/` → sivustolla näytettävät kuvat
- `OpenFreeMap` → karttapohja
- `Finna / KYPPi` → käyttäjän klikkaamat lähde- ja lisätietolinkit

### Tekniset muistiinpanot GeoLibrestä

- **GeoLibre ei näyttänyt kaikkia kuvia vakaasti.** → Kuvat siirrettiin Finna/KYPPi-suoralinkeistä omaan GitHub Pages `images/` -hakemistoon.
- **Base64-kuvat tekivät `.geolibre.json`-tiedostosta valtavan ja hankalan muokata.** → Kuvakentät vaihdettiin tavallisiksi HTTPS-kuvalinkeiksi.
- **Pystysuuntaiset kuvat rajautuivat GeoLibren leveissä kuvalohkoissa.** → Tehtiin erillisiä GeoLibre/web-versioita, joissa koko kuva mahtuu leveään kehykseen ilman varsinaisen kuvasisällön leikkaamista.
- **Pitkät otsikot katkeavat kapealla näytöllä.** → GeoLibre-versiossa otsikkopalkki pidetään lyhyenä ja pidempi tarinallinen otsikko sijoitetaan tekstin alkuun.
- **JSON rikkoutui helposti käsin muokattaessa.** → Muutokset rajattiin mahdollisimman pieniksi. Markdown-linkkejä ei käytetä JSONin URL-kentissä, vaan niissä käytetään paljaita URL-osoitteita.
- **Sama tieto esiintyi useissa JSON/GeoJSON-varatiedostoissa.** → Yksi `.geolibre.json` toimii master-projektina; muut tiedostot ovat lähinnä varmuus- ja työaineistoa.
- **Kuvaoikeudet vaihtelevat lähteittäin.** → Kuvaaja-, vuosi-, organisaatio-, lähde- ja lisenssitiedot on koottu tämän README-tiedoston kuvaosioon.
- **GeoLibren Present/embed-näkymällä on typografisia ja asetteluun liittyviä rajoituksia.** → GeoLibreä käytetään kartan, kohdekorttien ja tarinasiirtymien esittämiseen. Tarvittaessa ulkoasua voidaan myöhemmin viimeistellä itsenäisessä HTML-versiossa.

# Kuvien lähteet ja käyttöoikeudet

<sub>Verkkosivulla käytetyt kuvat on pienennetty ja optimoitu verkkokäyttöön. Alkuperäisen kuvan sisältöä ei ole tarkoituksellisesti muutettu; GeoLibreä varten joihinkin kuviin on lisätty kehystilaa kuvasuhteen sovittamiseksi.</sub>

<sub><strong>01_eura_luistari.jpg</strong><br>
Leena Koivisto · 2009 · Satakunnan Museo · CC BY 4.0<br>
https://www.finna.fi/Record/museovirasto.6F835FF3661121A7538996C48C5279EF?sid=5451478102</sub>

<sub><strong>02_eura_emanta_geolibre.jpg</strong><br>
Matti Bergström · vuosi ei ilmoitettu lähdetietueessa · Museovirasto · CC BY 4.0<br>
https://www.finna.fi/Record/musketti.M012:AKD7157:1</sub>

<sub><strong>03_kauttua_linnavuori.jpg</strong><br>
Leena Koivisto · 2011 · Satakunnan Museo · CC BY 4.0<br>
https://satakunnanmuseo.finna.fi/Record/satakunnanmuseo.44EF6E1E-75FE-4DA5-BB43-541572C337A2?sid=5451393709</sub>

<sub><strong>04_tupamaki_rautakuona.jpg</strong><br>
Teija Tiitinen · 2021 · Museovirasto · CC BY 4.0<br>
https://finna.fi/Record/museovirasto.013353e5-d960-40e3-8a7d-99fe91eb5cb2?sid=5451487213</sub>

<sub><strong>05_koylio_lallin_kalmisto.jpg</strong><br>
A. Hackman · 1925 · Museovirasto / Kulttuuriympäristön palveluikkuna (KYPPi)<br>
https://www.kyppi.fi/to.aspx?id=129.130352</sub>

<sub><strong>06_tuhkanummi.jpg</strong><br>
Teemu Väisänen · 2019 · Satakunnan Museo · CC BY 4.0<br>
https://www.finna.fi/Record/satakunnanmuseo.7D6C0753-9E1E-41AE-BB9A-40D597753CFE?sid=5451490915</sub>

<sub><strong>07_villionsuvanto_liesi.jpg</strong><br>
Leena Koivisto · 2019 · Satakunnan Museo · CC BY 4.0<br>
https://www.finna.fi/Record/satakunnanmuseo.35BBE115-BF9A-49D9-BF26-D7D9114DE840?sid=5451492481</sub>

<sub><strong>08_peravainionmaki.jpg</strong><br>
Teemu Väisänen · 2019 · Satakunnan Museo · CC BY 4.0<br>
https://www.finna.fi/Record/satakunnanmuseo.1B849E63-5698-4CFD-85CB-AD848F3457ED?sid=5451494515</sub>

<sub><strong>10_hankkasmaki_kupurasolki.jpg</strong><br>
Teemu Väisänen · 2024 · Satakunnan Museo · CC BY 4.0<br>
https://www.finna.fi/Record/satakunnanmuseo.087e7fbf-db2b-4df9-b53f-230ef99fc9e0?sid=5451496576</sub>

<sub><strong>11_lopetus_hankkasmaki_maisema_geolibre.jpg</strong><br>
Teemu Väisänen · 2025 · Muinaistutkija 3/2025 Väisänen & Kirkinen / Suomen arkeologinen seura<br>
https://doi.org/10.61258/mt.173127</sub>
