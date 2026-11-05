---
layout: default
title: Design system
permalink: /design-system/
hero_title: Design system
hero_text: "Bouwstenen voor de site van de Standaard voor Publieke Code. Het design system erft van drie merken: [Opensourcewerken.nl](https://opensourcewerken.nl) voor open samenwerken, [Code for NL](https://www.codefor.nl) als thuisbasis en [Standard for Public Code](https://www.standardforpubliccode.org) voor opensource werken."
---

## Merkenboom

De Standaard voor Publieke Code heeft twee kanten: de menselijke kant en de beschrijvende kant. Het design system erft van een merk per kant. Daartussen staat Code for NL, de community waar de Nederlandse vertaling thuis is. Elk token en elk component op deze pagina laat zien waar het vandaan komt.

<div class="brand-tree">
  <div class="brand-tree__parents">
    <div class="brand-node brand-node--osw">
      <div class="brand-node__kicker">Bronmerk 1 · <code>--osw-*</code></div>
      <div class="brand-node__title"><a href="https://opensourcewerken.nl">Opensourcewerken.nl</a></div>
      <div class="brand-node__motto">Open samenwerken</div>
      <p>De menselijke kant: samen organiseren, meetups, community of practice.</p>
      <ul>
        <li>Kleur: paars en roze</li>
        <li>Lettergroottes, hoeken en schaduwen (niet het lettertype)</li>
        <li>Componenten om mee te doen: header, banner, kaarten, knoppen, widgets</li>
      </ul>
    </div>
    <div class="brand-node brand-node--cfnl">
      <div class="brand-node__kicker">Bronmerk 2 · <code>--cfnl-*</code></div>
      <div class="brand-node__title"><a href="https://www.codefor.nl">Code for NL</a></div>
      <div class="brand-node__motto">Thuisbasis</div>
      <p>De community waar de Nederlandse vertaling thuis is: samenwerken aan een open, eerlijke en inclusieve digitale overheid.</p>
      <ul>
        <li>Manieren van meedoen: meedoen, meeleren, meekijken</li>
        <li>Kerncijfers van de community</li>
        <li>Afzender-vermelding met het oranje woordmerk</li>
        <li>Niet: Anton en Roboto, die botsen met de leesbaarheidsregels</li>
      </ul>
    </div>
    <div class="brand-node brand-node--sfpc">
      <div class="brand-node__kicker">Bronmerk 3 · <code>--sfpc-*</code></div>
      <div class="brand-node__title"><a href="https://www.standardforpubliccode.org">Standard for Public Code</a></div>
      <div class="brand-node__motto">Opensource werken</div>
      <p>De beschrijvende kant: hergebruik, leesbaarheid, kwaliteit.</p>
      <ul>
        <li>Zwarte tekst op wit, grijze achtergrond buiten de pagina</li>
        <li>Links altijd onderstreept, de kleur van de streep geeft de status</li>
        <li>Lettertypen: Mulish voor koppen, systeemlettertype voor tekst</li>
        <li>Maximale regellengte</li>
        <li>Componenten om te beschrijven: eisen-lijsten, printbaar op A4</li>
      </ul>
    </div>
  </div>
  <div class="brand-tree__join" aria-hidden="true"></div>
  <div class="brand-tree__stem" aria-hidden="true"></div>
  <div class="brand-node brand-node--self">
    <div class="brand-node__kicker">Eigen merk · <code>--color-*</code>, <code>--font-*</code>, <code>--space-*</code> …</div>
    <div class="brand-node__title">Standaard voor Publieke Code</div>
    <p>Componenten gebruiken alleen deze merktokens, nooit direct de tokens van een bronmerk.</p>
  </div>
  <div class="brand-tree__stem" aria-hidden="true"></div>
  <nav class="atomic-chain" aria-label="Lagen van het design system">
    <a href="#tokens">Tokens</a><span aria-hidden="true">→</span>
    <a href="#atomen">Atomen</a><span aria-hidden="true">→</span>
    <a href="#moleculen">Moleculen</a><span aria-hidden="true">→</span>
    <a href="#organismen">Organismen</a><span aria-hidden="true">→</span>
    <a href="#templates">Templates</a><span aria-hidden="true">→</span>
    <a href="#paginas">Pagina's</a>
  </nav>
</div>

### Wie wint bij een conflict?

| Onderwerp | Opensourcewerken.nl | Code for NL | Standard for Public Code | Keuze |
|---|---|---|---|---|
| Lopende tekst | Paars en zwart | Grijs | Altijd zwart | <span class="origin origin--sfpc">sfpc</span> Zwart, want leesbaarheid gaat voor |
| Koppen | Paars | Rood, Anton, hoofdletters | Zwart | <span class="origin origin--osw">osw</span> Paars, zodat de pagina herkenbaar en warm blijft |
| Links | Paars | Groen | Zwart met een gekleurde onderstreping | <span class="origin origin--sfpc">sfpc</span> Zwart, met een blauwe streep voor onbezocht en een paarse (osw) streep voor bezocht |
| Lettertype | Rijksoverheid Sans | Anton en Roboto (Google Fonts) | Mulish voor koppen, systeemlettertype voor tekst | <span class="origin origin--sfpc">sfpc</span> Mulish en systeemlettertype. Rijksoverheid Sans is alleen voor de Rijksoverheid, en wij zijn geen overheid |
| Regellengte | Niet vastgelegd | Niet vastgelegd | Maximaal ongeveer 35em | <span class="origin origin--sfpc">sfpc</span> `--measure` |
| Accentkleur | Roze | Oranje, rood, groen | Geen | <span class="origin origin--osw">osw</span> Roze. Oranje <span class="origin origin--cfnl">cfnl</span> alleen in de afzender |
| Meedoen-kleuren | Geen | Groen, blauw, paars | Geen | <span class="origin origin--cfnl">cfnl</span> Alleen als stip of rand, want groen en blauw hebben te weinig contrast voor tekst |

### Bestanden

| Laag | Bestand |
|---|---|
| Bronmerk 1 | `_sass/tokens/_opensourcewerken.scss` |
| Bronmerk 2 | `_sass/tokens/_codefornl.scss` |
| Bronmerk 3 | `_sass/tokens/_standardforpubliccode.scss` |
| Eigen merk | `_sass/tokens/_spc.scss` |
| Atomen, moleculen, organismen | `_sass/atoms/`, `_sass/molecules/`, `_sass/organisms/` |
| Templates | `_layouts/` en `_sass/templates/` |
| Alles samen | `assets/css/design-system.scss` |

## Tokens

### Kleur

Paars is de primaire kleur en roze het accent. Zet op roze altijd paarse tekst. Witte tekst op roze heeft te weinig contrast.

<div class="swatches">
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-primary)"></div><div class="swatch__meta"><strong>Primair</strong><code>--color-primary</code><code>#42145f</code><span class="origin origin--osw">osw</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-accent)"></div><div class="swatch__meta"><strong>Accent / header</strong><code>--color-accent</code><code>#f092cd</code><span class="origin origin--osw">osw</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-primary-hover)"></div><div class="swatch__meta"><strong>Primair hover</strong><code>--color-primary-hover</code><code>#2e0d43</code><span class="origin origin--self">eigen</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-primary-subtle)"></div><div class="swatch__meta"><strong>Primair subtiel</strong><code>--color-primary-subtle</code><code>#f3edf7</code><span class="origin origin--self">eigen</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-accent-subtle)"></div><div class="swatch__meta"><strong>Accent subtiel</strong><code>--color-accent-subtle</code><code>#fce9f5</code><span class="origin origin--self">eigen</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-text)"></div><div class="swatch__meta"><strong>Tekst</strong><code>--color-text</code><code>#000000</code><span class="origin origin--sfpc">sfpc</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-text-muted)"></div><div class="swatch__meta"><strong>Tekst gedempt</strong><code>--color-text-muted</code><code>#5c5c5c</code><span class="origin origin--self">eigen</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-surface)"></div><div class="swatch__meta"><strong>Pagina</strong><code>--color-surface</code><code>#ffffff</code><span class="origin origin--sfpc">sfpc</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-background)"></div><div class="swatch__meta"><strong>Buiten de pagina</strong><code>--color-background</code><code>#f5f5f5</code><span class="origin origin--sfpc">sfpc</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-meedoen)"></div><div class="swatch__meta"><strong>Meedoen</strong><code>--color-meedoen</code><code>#97bd2e</code><span class="origin origin--cfnl">cfnl</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-meeleren)"></div><div class="swatch__meta"><strong>Meeleren</strong><code>--color-meeleren</code><code>#348faa</code><span class="origin origin--cfnl">cfnl</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-meekijken)"></div><div class="swatch__meta"><strong>Meekijken</strong><code>--color-meekijken</code><code>#56165c</code><span class="origin origin--cfnl">cfnl</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-endorsement-highlight)"></div><div class="swatch__meta"><strong>Afzender</strong><code>--color-endorsement-highlight</code><code>#eb8c3a</code><span class="origin origin--cfnl">cfnl</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-link-underline)"></div><div class="swatch__meta"><strong>Linkstreep</strong><code>--color-link-underline</code><code>#0000ff</code><span class="origin origin--sfpc">sfpc</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-link-visited-underline)"></div><div class="swatch__meta"><strong>Linkstreep bezocht</strong><code>--color-link-visited-underline</code><code>#42145f</code><span class="origin origin--osw">osw</span> <span class="origin origin--sfpc">sfpc</span></div></div>
  <div class="swatch"><div class="swatch__chip" style="background: var(--color-link-internal-underline)"></div><div class="swatch__meta"><strong>Linkstreep binnen pagina</strong><code>--color-link-internal-underline</code><code>#a9a9a9</code><span class="origin origin--sfpc">sfpc</span></div></div>
</div>

### Typografie

Koppen gebruiken Mulish en lopende tekst het systeemlettertype van het apparaat <span class="origin origin--sfpc">sfpc</span>. Opensourcewerken.nl gebruikt Rijksoverheid Sans, maar dat lettertype is alleen voor de Rijksoverheid. Wij zijn geen overheid, dus we nemen het niet over. De lettergroottes komen van opensourcewerken.nl <span class="origin origin--osw">osw</span>. De maximale regellengte (`--measure`) komt van de Standard for Public Code <span class="origin origin--sfpc">sfpc</span>.

<div class="stack">
  <p class="heading-enormous">Enorm 50/62</p>
  <p class="heading-huge">Heel groot 42/54</p>
  <p class="heading-large">Groot 30/38</p>
  <p class="heading-normal">Normaal 24/30</p>
  <p class="heading-small">Klein 20/28</p>
  <p class="text-large">Tekst groot 18/26: publieke organisaties ontwikkelen en onderhouden samen software en beleid.</p>
  <p>Tekst normaal 16/24: de Standaard voor Publieke Code is een set criteria die publieke organisaties ondersteunt.</p>
  <p class="text-small text-muted">Tekst klein 14/20, gedempt: metadata, bijschriften en voetnoten.</p>
</div>

### Vorm en schaduw

Hoeken en schaduwen komen van opensourcewerken.nl <span class="origin origin--osw">osw</span>.

<div class="demo-row">
  <figure><div class="demo-box" style="border-radius: var(--corner-sm); box-shadow: var(--shadow-hard-outside)"></div><figcaption><code>--corner-sm</code> 4px</figcaption></figure>
  <figure><div class="demo-box" style="border-radius: var(--corner-md); box-shadow: var(--shadow-hard-outside)"></div><figcaption><code>--corner-md</code> 6px</figcaption></figure>
  <figure><div class="demo-box" style="box-shadow: var(--shadow-hard-outside)"></div><figcaption><code>--corner-lg</code> 8px</figcaption></figure>
  <figure><div class="demo-box" style="border-radius: var(--corner-xl); box-shadow: var(--shadow-hard-outside)"></div><figcaption><code>--corner-xl</code> 20px</figcaption></figure>
  <figure><div class="demo-box" style="box-shadow: var(--shadow-soft-bottom)"></div><figcaption><code>--shadow-soft-bottom</code></figcaption></figure>
  <figure><div class="demo-box" style="box-shadow: var(--shadow-soft-center)"></div><figcaption><code>--shadow-soft-center</code></figcaption></figure>
</div>

### Ruimte

Een raster van 4px <span class="origin origin--self">eigen</span>.

| Token | Waarde | Voorbeeld |
|---|---|---|
| `--space-1` | 4px | <span class="demo-bar" style="width: 4px"></span> |
| `--space-2` | 8px | <span class="demo-bar" style="width: 8px"></span> |
| `--space-3` | 12px | <span class="demo-bar" style="width: 12px"></span> |
| `--space-4` | 16px | <span class="demo-bar" style="width: 16px"></span> |
| `--space-5` | 24px | <span class="demo-bar" style="width: 24px"></span> |
| `--space-6` | 32px | <span class="demo-bar" style="width: 32px"></span> |
| `--space-7` | 48px | <span class="demo-bar" style="width: 48px"></span> |
| `--space-8` | 64px | <span class="demo-bar" style="width: 64px"></span> |

## Atomen

De kleinste bouwstenen. Je kunt ze niet verder opdelen zonder dat ze hun betekenis verliezen.

### Link <span class="origin origin--sfpc">sfpc</span>

Een link is zwart en altijd onderstreept. De kleur van de streep laat zien [waar een link naartoe gaat](#link-sfpc): blauw als je de pagina nog niet hebt bezocht, paars als je er al was, grijs voor een plek op dezelfde pagina. Voorbeeld: [de Nederlandse vertaling](https://codefor.nl/community-translations-standard/nl/).

### Knop <span class="origin origin--osw">osw</span>

<div class="button-row">
  <a class="button button--primary" href="#knop-osw">Primair</a>
  <a class="button button--secondary" href="#knop-osw">Secundair</a>
  <a class="button button--accent" href="#knop-osw">Accent</a>
</div>

<div class="button-row demo-dark">
  <a class="button button--on-dark" href="#knop-osw">Op donker</a>
  <a class="button button--accent" href="#knop-osw">Accent op donker</a>
</div>

### Label <span class="origin origin--osw">osw</span>

<p><span class="tag">Criterium</span> <span class="tag tag--accent">Community call</span></p>

### Meedoen-label <span class="origin origin--cfnl">cfnl</span>

De drie manieren om mee te doen, zoals op codefor.nl. De kleur zit in de stip, de tekst blijft zwart.

<p><span class="tag tag--meedoen">Meedoen</span> <span class="tag tag--meeleren">Meeleren</span> <span class="tag tag--meekijken">Meekijken</span></p>

### Eis-woord <span class="origin origin--sfpc">sfpc</span>

<p><span class="keyword keyword--must">Moet</span> · <span class="keyword keyword--should">Zou moeten</span> · <span class="keyword keyword--optional">Optioneel</span></p>

### Label en invoerveld <span class="origin origin--self">eigen</span>

<div class="demo-row">
  <span class="label">Label</span>
  <input class="input" type="text" aria-label="Voorbeeld van een invoerveld" placeholder="Invoerveld">
</div>

### Woordmerk <span class="origin origin--osw">osw</span>

<div class="demo-row" style="padding: var(--space-5); background: var(--color-accent); border-radius: var(--corner-lg)">
  <span class="wordmark">Standaard voor Publieke Code</span>
</div>

## Moleculen

Een molecuul is een kleine groep atomen die samen één taak doen.

### Formulierveld <span class="origin origin--self">eigen</span>

Label + invoerveld.

<div class="field">
  <label class="label" for="demo-email">E-mailadres</label>
  <input class="input" id="demo-email" type="email" placeholder="naam@organisatie.nl">
</div>

### Knoppengroep <span class="origin origin--osw">osw</span>

Knop + knop.

<div class="button-row">
  <a class="button button--primary" href="#knoppengroep-osw">Meld je aan</a>
  <a class="button button--secondary" href="#knoppengroep-osw">Lees meer</a>
</div>

### Melding <span class="origin origin--self">eigen</span>

Een gekleurd blok met tekst en links.

<div class="stack">
  <div class="alert">Elke maand is er een community call. Meld je aan voor de <a href="#melding-eigen">nieuwsbrief</a>, dan krijg je de uitnodiging.</div>
  <div class="alert alert--accent">De presentatie van de criteria is online te bekijken.</div>
</div>

### Linklijst <span class="origin origin--osw">osw</span>

Een lijst van links, elk met een pijl.

<div class="widget" style="max-width: 400px">
  <ul class="link-list">
    <li><a href="#linklijst-osw">Lees de NL vertaling</a></li>
    <li><a href="#linklijst-osw">Bekijk de presentatie</a></li>
  </ul>
</div>

### Afzender <span class="origin origin--cfnl">cfnl</span>

Tekst + Code for NL-woordmerk, in de stijl van het logo op codefor.nl. Te gebruiken als een pagina een afzender nodig heeft.

<div class="demo-dark">
  <a class="endorsement" href="https://www.codefor.nl" style="color: var(--color-on-primary)">Thuisbasis: <span class="endorsement__mark">Code for <span class="endorsement__highlight">NL</span></span></a>
</div>

## Organismen

Een organisme is een herkenbaar deel van een pagina, opgebouwd uit moleculen en atomen.

### Banner <span class="origin origin--osw">osw</span>

Bovenaan elke pagina: een paarse balk met een kop, inleiding en een knoppengroep. Op de site staat er een foto achter, met een paarse overloop van links naar rechts zodat de tekst leesbaar blijft. De standaardfoto staat in `_config.yml` (`hero_image`) en is per pagina te overschrijven in de front matter.

<div class="hero" style="padding: var(--space-6) var(--space-5); border-radius: var(--corner-lg)">
  <h1>Samen publieke code maken</h1>
  <p>Doe mee met de community rond de Standaard voor Publieke Code.</p>
  <div class="button-row">
    <a class="button button--accent" href="#banner-osw">Meld je aan</a>
    <a class="button button--on-dark" href="#banner-osw">Lees de standaard</a>
  </div>
</div>

### Kaart <span class="origin origin--osw">osw</span>

Afbeelding + titel + tekst + actie. Gebruik de uitgelichte variant voor het belangrijkste item.

<div class="card-grid">
  <article class="card card--featured">
    <img class="card__image" src="https://avatars.githubusercontent.com/u/165153351?s=400&v=4" alt="">
    <div class="card__body">
      <span><span class="tag tag--accent">Uitgelicht</span></span>
      <h4 class="card__title">Uitgelichte kaart</h4>
      <p>Voor het belangrijkste item op een pagina. Krijgt een roze rand.</p>
      <div class="card__footer"><a class="button button--primary" href="#kaart-osw">Actie</a></div>
    </div>
  </article>
  <article class="card">
    <img class="card__image" src="https://avatars.githubusercontent.com/u/165153351?s=400&v=4" alt="">
    <div class="card__body">
      <h4 class="card__title">Standaardkaart</h4>
      <p>Witte kaart met zachte schaduw, hoeken van 8px en een paarse titel.</p>
      <div class="card__footer"><a href="#kaart-osw">Tekstlink als actie</a></div>
    </div>
  </article>
</div>

Met een manier van meedoen <span class="origin origin--cfnl">cfnl</span> krijgt de kaart een gekleurde bovenrand:

<div class="card-grid">
  <article class="card card--meedoen"><div class="card__body"><span><span class="tag tag--meedoen">Meedoen</span></span><h4 class="card__title">Pas de standaard toe</h4><p>Toets je eigen codebase aan de criteria.</p></div></article>
  <article class="card card--meeleren"><div class="card__body"><span><span class="tag tag--meeleren">Meeleren</span></span><h4 class="card__title">Community call</h4><p>Elke maand ervaringen delen met andere organisaties.</p></div></article>
  <article class="card card--meekijken"><div class="card__body"><span><span class="tag tag--meekijken">Meekijken</span></span><h4 class="card__title">Nieuwsbrief</h4><p>Blijf op de hoogte zonder dat je meteen hoeft mee te doen.</p></div></article>
</div>

### Kerncijfers <span class="origin origin--cfnl">cfnl</span>

Grote getallen die laten zien hoe groot de community is. De getallen hieronder zijn voorbeelden.

<ul class="stats">
  <li class="stats__item"><span class="stats__number">16</span><span class="stats__label">criteria in de standaard</span></li>
  <li class="stats__item"><span class="stats__number">12</span><span class="stats__label">community calls per jaar</span></li>
  <li class="stats__item"><span class="stats__number">3</span><span class="stats__label">manieren van meedoen</span></li>
</ul>

### Community-blok <span class="origin origin--cfnl">cfnl</span> <span class="origin origin--osw">osw</span>

De community "Werken aan Publieke Code" met de twee manieren om mee te doen, onder elkaar in een opvallend roze blok: de meetup en de nieuwsbrief. Op de homepage staat het in de rechterkolom, op mobiel boven de documenten. Gebruik `{% raw %}{% include community.html %}{% endraw %}`. De teksten staan in `_data/community.yaml`.

<div style="max-width: 360px">
<div class="community">
  <h4 class="community__title">Werken aan Publieke Code</h4>
  <ul class="community__items">
    <li class="community__item"><span class="community__kicker">Meetup</span><span class="community__text">Kom naar de volgende meetup</span><a class="button button--primary" href="#community-blok-cfnl-osw">Bekijk de events <span aria-hidden="true">→</span></a></li>
    <li class="community__item"><span class="community__kicker">Blijf op de hoogte</span><span class="community__text">Meld je aan voor de nieuwsbrief</span><a class="button button--primary" href="#community-blok-cfnl-osw">Meld je aan <span aria-hidden="true">→</span></a></li>
  </ul>
</div>
</div>

### Documentenlijst <span class="origin origin--sfpc">sfpc</span>

Documenten als lijst in plaats van kaarten: titel, taal, beschrijving en een actie. De hele rij is klikbaar. De documenten op de homepage staan in `_data/documents.yaml`.

<ul class="document-list">
  <li><a class="document" href="#documentenlijst-sfpc"><span class="document__title">Standaard voor Publieke Code (NL) <span class="tag">NL</span></span><span class="document__description">Nederlandse vertaling van de Standaard voor Publieke Code.</span><span class="document__cta">Lees online</span></a></li>
  <li><a class="document" href="#documentenlijst-sfpc"><span class="document__title">Standard for Public Code (upstream) <span class="tag">EN</span></span><span class="document__description" lang="en">The Standard for Public Code is a set of criteria.</span><span class="document__cta" lang="en">Read online</span></a></li>
</ul>

### Widget <span class="origin origin--osw">osw</span>

Titel + linklijst, zoals het blok "Direct naar" op opensourcewerken.nl. Met `link-list--described` krijgt elke link een korte uitleg eronder. Zo staat "Meer manieren om mee te doen" op de homepage, onder het community-blok.

<div class="widget" style="max-width: 400px">
  <div class="widget__title">Direct naar</div>
  <ul class="link-list">
    <li><a href="#widget-osw">Lees de NL vertaling</a></li>
    <li><a href="#widget-osw">Meld je aan voor de nieuwsbrief</a></li>
    <li><a href="#widget-osw">Bekijk de presentatie</a></li>
  </ul>
</div>

### Eisen-lijst <span class="origin origin--sfpc">sfpc</span>

De lijst met eisen bij elk criterium van de standaard. Elke eis begint met een eis-woord. De teksten hieronder zijn voorbeelden.

<ul class="requirements">
  <li>Alle broncode die in gebruik is <span class="keyword keyword--must">moet</span> openbaar gepubliceerd zijn.</li>
  <li>De broncode <span class="keyword keyword--should">zou moeten</span> gepubliceerd worden voordat hij in gebruik genomen wordt.</li>
  <li>Een changelog bijhouden is <span class="keyword keyword--optional">optioneel</span>.</li>
</ul>

### Aftiteling <span class="origin origin--self">eigen</span>

Credits zoals aan het eind van een film: een zwarte achtergrond, één gecentreerde kolom en per sectie een rol met de namen onder elkaar. Logo's zijn wit, zonder blokje eromheen. Een naam zonder logo is ook goed. De namen komen uit `_data/credits.yaml`, de HTML uit `_includes/credits.html`. Gebruik voor een ministerie geen Rijkslogo, want dat is alleen voor de overheid zelf.

Een nieuwe naam toevoegen:

```yaml
- role: Organisatie meetups
  credits:
    - name: Naam van de organisatie of persoon
      url: https://example.org
      logo: /assets/img/credits/naam.png   # optioneel: wit logo, transparante achtergrond
```

### Footer <span class="origin origin--self">eigen</span>

Onderaan elke pagina: de aftiteling op zwart.

## Templates

Een template is een paginaskelet zonder echte inhoud.

| Template | Bestand | Opbouw |
|---|---|---|
| `default` | `_layouts/default.html` | Banner (als `hero_title` gezet is) → inhoud (`.prose`) → footer met aftiteling |

Voor een pagina met een rechterkolom gebruik je `.sidebar-layout` met `__aside` (eerst in de HTML, op mobiel bovenaan) en `__main`.

Een nieuwe pagina is een Markdown-bestand met deze front matter:

```yaml
---
layout: default
title: Paginatitel
hero_title: Kop in de banner      # optioneel
hero_text: "Inleiding, met **Markdown**"  # optioneel
---
```

## Pagina's

Een pagina is een template met echte inhoud.

| Pagina | Bestand | Template |
|---|---|---|
| [Startpagina](/) | `index.html` | `default`, met banner, documentenlijst (`_data/documents.yaml`) en community-blok in de rechterkolom (`_data/community.yaml`) |
| Design system | `design-system.md` | `default`, met banner en Markdown-inhoud |
