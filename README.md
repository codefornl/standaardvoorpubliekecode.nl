# standaardvoorpubliekecode.nl

Community-website voor de Standaard voor Publieke Code. Een Jekyll-site, gepubliceerd via GitHub Pages.

## Lokaal draaien

```sh
jekyll serve
```

De site staat dan op http://localhost:4000. Het design system staat op `/design-system/`.

## Inhoud aanpassen

| Wat | Bestand |
|---|---|
| Community-blok (meetup en nieuwsbrief) | `_data/community.yaml` |
| Documenten op de homepage | `_data/documents.yaml` |
| Aftiteling in de footer | `_data/credits.yaml` (logo's: wit PNG in `assets/img/credits/`) |
| Banner-foto | `hero_image` in `_config.yml`, of per pagina in de front matter |

## Opbouw

Het design system erft van drie merken (Opensourcewerken.nl, Code for NL en Standard for Public Code) en is opgebouwd volgens atomic design:

```
_sass/
  tokens/      bronmerken (--osw-*, --cfnl-*, --sfpc-*) en het eigen merk (_spc.scss)
  base/        breekpunten, reset, basisstijl
  atoms/       link, knop, label, …
  molecules/   formulierveld, melding, linklijst, …
  organisms/   banner, community-blok, documentenlijst, aftiteling, …
  templates/   container, raster, prose
  docs/        alleen voor de design system-pagina
assets/css/design-system.scss   laadt alles in deze volgorde
_layouts/default.html           het paginaskelet
_includes/                      community-blok en aftiteling
```

Componenten gebruiken alleen de tokens van het eigen merk, nooit direct die van een bronmerk. Zie `/design-system/` voor alle tokens en componenten.
