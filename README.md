# 🥏 Disc Golf GPS Distance Tracker

Selaimessa toimiva helppokäyttöinen web-sovellus frisbeegolf-heittojen pituuden mittaamiseen laitteen oman GPS-paikannuksen avulla. Sovelluksella voit mitata heittojesi etäisyyden ja pitää kirjaa käytetyistä kiekoista.

## ✨ Ominaisuudet

- **Mittaa heiton pituus GPS:llä:** Aseta aloituspiste (tiipaikka/heittoalue) ja kävele kiekolle nähdäksesi etäisyyden reaaliajassa.
- **Kiekon valinta & seuranta:** Kirjaa mitä kiekkoa käytit heitossa (esim. draiveri, midari, putteri).
- **Tarkka paikannus:** Hyödyntää HTML5 Geolocation API:a ja reaaliaikaista paikan seurantaa.
- **Mobiiliystävällinen:** Suunniteltu toimimaan sujuvasti suoraan älypuhelimen selaimella kentällä oltaessa.
- **Ei erillistä asennusta:** Toimii kevyenä Web Appina ilman raskaita sovelluskauppa-asennuksia.

## 🛠️ Teknologiat

- **HTML5 & CSS3** – Rakenne ja responsiivinen käyttöliittymä
- **JavaScript (ES6+)** – Etäisyyslaskenta ja GPS-logiikka
- **Geolocation API** – Laitteen sijaintitietojen hyödyntäminen

## 📐 Miten etäisyys lasketaan?

Mittaus perustuu kahden koordinaatin (aloituspiste ja nykyinen sijainti) väliseen etäisyyteen, joka lasketaan **Haversinen kaavalla**:

$$d = 2r \arcsin\left(\sqrt{\sin^2\left(\frac{\Delta \phi}{2}\right) + \cos(\phi_1) \cos(\phi_2) \sin^2\left(\frac{\Delta \lambda}{2}\right)}\right)$$

Kaava ottaa huomioon maapallon kaarevuuden ja antaa tarkan etäisyyden metreinä.

## 🚀 Käyttöohje

1. **Avaa sovellus** älypuhelimesi selaimessa (varmista, että GPS/sijaintipalvelut ovat päällä).
2. **Salli sijaintitiedot**, kun selain pyytää lupaa.
3. **Aseta aloituspiste:** Seiso tiipaikalla ja paina *Mark Throw* / *Aseta aloituspiste* -painiketta.
4. **Valitse kiekko:** Kirjaa käytetty kiekko listasta tai syötä uusi kiekko.
5. **Kävele kiekolle:** Näet etäisyyden päivittyvän reaaliajassa näytöllä.
6. **Tallenna heitto:** Kun pääset kiekolle, lukitse tulos ja tallenna heitto historiaan.

## 💻 Paikallinen kehitys (Local Setup)

Jos haluat ajaa projektia paikallisesti tai kehittää sitä edelleen:

1. Kloonaa repositorio:
   ```bash
   git clone [https://github.com/Pekx97/disc-golf-gps.git](https://github.com/Pekx97/disc-golf-gps.git)
