# KanFit workshops

Twee online workshops van het **KanFit-project** (Universiteit Gent), gefinancierd
door Kom op tegen Kanker (KOTK) en het Fonds Wetenschappelijk Onderzoek (FWO).

| Workshop | Voor wie | Link |
|----------|----------|------|
| **Workshop voor hulpverleners** | Artsen, verpleegkundigen, kinesitherapeuten en andere hulpverleners in de oncologie | [Start de workshop](https://stvsever.github.io/Workshops_KanFit/hulpverleners/) |
| **Jouw ervaring telt mee** | Mensen die borstkanker, prostaatkanker of darmkanker hebben gehad | [Start de workshop](https://stvsever.github.io/Workshops_KanFit/kankeroverlevers/) |

Overzichtspagina: <https://stvsever.github.io/Workshops_KanFit/>

Elke workshop duurt ongeveer een uur. U kan tussendoor pauzeren en later verdergaan.

Vragen of problemen? Contacteer **Emma Tack**, [emma.tack@ugent.be](mailto:emma.tack@ugent.be).

---

## Uw antwoorden blijven op uw eigen toestel

Dit is het belangrijkste om te weten voordat u begint.

**Er is geen server.** Deze workshops zijn gewone webpagina's zonder achterliggende toepassing.
GitHub Pages levert enkel het bestand af aan uw browser en krijgt daarna niets meer te zien. Er is
geen database, geen account, geen login, geen cookiebanner en geen bezoekersteller.

**Uw antwoorden worden nergens verstuurd.** Alles wat u aanklikt of typt, wordt opgeslagen in de
lokale opslag (`localStorage`) van uw eigen browser, op uw eigen toestel. Dat gebeurt automatisch
terwijl u invult, zodat u kan pauzeren en later op hetzelfde toestel verdergaan.

**Het onderzoeksteam ontvangt pas iets wanneer u het zelf verstuurt.** Op het laatste scherm klikt u
op *Antwoorden opslaan als bestand (JSON)*. Dat bestand komt in uw map Downloads terecht. U mailt het
zelf als bijlage naar [emma.tack@ugent.be](mailto:emma.tack@ugent.be). Zolang u dat niet doet, heeft
het onderzoeksteam niets van u.

**De pagina praat na het laden met niemand.** De tekst, de inhoud uit de kennisbron en de afbeelding
zitten allemaal in het HTML-bestand zelf. Er worden geen lettertypes, scripts, afbeeldingen of
statistieken van elders opgehaald. U kan de pagina zelfs offline invullen.

**U kan alles wissen.** De knop *Wissen* bovenaan verwijdert al uw antwoorden uit de opslag van de
browser. Ook het legen van uw browsergegevens verwijdert ze.

**Weigert uw browser opslag, dan werkt de workshop nog steeds.** Sommige browsers laten geen site-
gegevens toe, en dat merkt u aan een oranje balk bovenaan de pagina. Uw antwoorden blijven dan enkel
bewaard zolang de pagina openstaat. Invullen en het bestand opslaan werken gewoon; enkel pauzeren en
later verdergaan lukt dan niet.

### Waar u wel op moet letten

* Uw antwoorden staan **per toestel en per browser**. Begint u op uw laptop en gaat u verder op uw
  gsm, dan staat daar een lege workshop. Rond een workshop dus af op hetzelfde toestel.
* Gebruikt u een **gedeelde of publieke computer**, klik dan op *Wissen* wanneer u klaar bent, of
  gebruik een privévenster. In een privévenster verdwijnen uw antwoorden wel zodra u het venster
  sluit, dus vul de workshop dan in één keer in en exporteer het bestand voor u afsluit.
* Wist u uw browsergegevens of gebruikt u een browser die dat automatisch doet, dan verdwijnen de
  antwoorden mee.

### Welke gegevens zitten in het geëxporteerde bestand

Uw antwoorden, uw toelichtingen, en de achtergrondvragen uit het onderzoeksprotocol (voor
hulpverleners: diploma, functie, jaren ervaring, frequentie van contact met kankeroverlevers; voor
deelnemers die kanker hebben gehad: diagnose, behandeling, tijd sinds het einde van de primaire
behandeling).

Het bestand is leesbaar zonder de pagina erbij: bij elk antwoord staat de vraag die gesteld werd, de
tekst van wat u beoordeeld hebt en het opschrift van de knop die u koos. U kan het dus zelf openen en
nalezen voor u het doorstuurt.

Uw naam, e-mailadres of andere rechtstreeks identificerende gegevens worden **nergens gevraagd** en
staan dus ook niet in het bestand. Uw e-mailadres is het onderzoeksteam natuurlijk wel bekend zodra u
het bestand doormailt; het team codeert de bestanden en verwerkt ze vertrouwelijk, conform de GDPR en
het gegevensbeschermingsbeleid van de UGent.

---

## Wat er in deze repository staat

Enkel de twee workshoppagina's en deze uitleg.

```
index.html                    overzichtspagina met een link naar beide workshops
hulpverleners/index.html      workshop voor hulpverleners
kankeroverlevers/index.html   workshop voor mensen die kanker hebben gehad
README.md                     dit bestand
.nojekyll                     GitHub Pages levert de bestanden ongewijzigd af
```

Elke workshop is **één op zichzelf staand HTML-bestand**. Alles zit erin: de opmaak, het gedrag, de
teksten, de inhoud uit de kennisbron en de projectafbeelding. Er is geen bouwstap, geen
afhankelijkheid en geen configuratie.

De onderzoekscode, de kennisbron en de analysescripts staan **niet** in deze repository. Die worden
apart bijgehouden; hier staan alleen de pagina's die de deelnemers te zien krijgen.

## Zelf openen zonder internet

Download deze repository (*Code* > *Download ZIP*), pak ze uit en open
`hulpverleners/index.html` of `kankeroverlevers/index.html` in een browser. Dat werkt volledig
offline en de opslag werkt precies hetzelfde.

## Hosten via GitHub Pages

*Settings* > *Pages* > *Build and deployment* > *Deploy from a branch* > branch `main`, map `/ (root)`.
Na een minuut staat de site op `https://stvsever.github.io/Workshops_KanFit/`.

## Technische noot

De pagina's zijn **gegenereerd**. Ze komen uit de bronrepository van het project, waar de teksten in
een apart tekstbestand per workshop staan en de inhoud uit de kennisbron wordt opgebouwd. Een
aanpassing gebeurt daar, waarna de pagina's opnieuw gebouwd en hierheen gekopieerd worden. Wie hier
rechtstreeks in een `index.html` schrijft, moet die wijziging dus laten overzetten naar de bron,
anders is ze bij de volgende bouw weer verdwenen.

De opslagsleutels in de browser zijn `coppercan_workshop_hv` en `coppercan_workshop_cs`; de
geëxporteerde bestanden heten `kanfit_workshop_hv_<datum>.json` en `kanfit_workshop_cs_<datum>.json`.
De pagina's werken in elke recente browser (Chrome, Firefox, Safari, Edge) op computer, tablet en gsm.
