# Ha developer,

Bij Studio Lemon ontwikkelen wij websites op basis van een bibliotheek aan slimme modules, aangevuld met maatwerk. Dat doen we voor directe opdrachtgevers maar ook als technisch- en UX-partner voor creatieve bureaus. We ontwikkelen op basis van WordPress en andere open source technieken, zoals PHP, JavaScript en HTML5/CSS.

## Wij zoeken

Hier komt een verhaal.

## Jij bent

De developer vanuit een ontwerp uit Sketch/Marvel/XD mobile-first kan omzetten naar herbruikbareHTML/SCSS/JS modules en zijn weg weet in het moderne development landschap. We verwachten geen full-stack experience van je, maar ervaring met veel van de onderstaande tooling of frameworks is zeker een pluspunt.

## Vereisten

- Ervaring met het maken van custom WordPress thema's
- Kennis van GIT
- kennis van SCSS
- Je hebt een lokale development omgeving
- Enige kennis van de commandline

## Nice to haves

- Ervaring met Composer
- Ervarning met YARN/NPM voor het installeren van de benodigde front-end frameworks en modules.
- Ervaring met webpack
- Eerder gewerkt met Twig of andere templating engine
- Ervarning met Bootstrap, we gebruiken voornamelijk het grid.

# Wij werken met:

Hieronder vind je een lijst met tools waar wij mee werken. Hoe meer ervaring je hebt met de onderstaande tools, des te sneller je aan de slag kan met onze projecten.

## WordPress op basis van Bedrock

Websites bouwen we dus op basis van WordPress. Om de standaard WordPress installatie te beveiligen gebruiken wij [Bedrock van root.io](https://roots.io/bedrock/), hier te vinden op [github](https://github.com/roots/bedrock).

Dit zorgt voor een beter beveiligde WordPress installatie met betere password hashing, de mogelijkheid om heel snel te switchen van Development modus met debugging, naar Staging met google indexatie uit, naar Production.

Daarnaast geeft het ons de mogelijkheid om WordPress onderdeel te maken van onze GIT repository. Een Bedrock based WordPress installtatie ziet er zo uit:

```shell
├── composer.json
├── config
│   ├── application.php
│   └── environments
│       ├── development.php
│       ├── staging.php
│       └── production.php
├── vendor
└── web
    ├── app
    │   ├── mu-plugins
    │   ├── plugins
    │   ├── themes
    |   │   └── **Studio Lemon custom Theme**
    │   └── uploads
    ├── wp-config.php
    ├── index.php
    └── wp
```

## Plugins

Bij Lemon gebruiken we zo min mogelijk plugins. De plugins die toch voor ieder project noodzakelijk zijn staan hieronder:

**Advanced Custom Fields** Custom fields doen we op basis van [Advanced Custom fields](https://www.advancedcustomfields.com/) met [JSON sync](https://www.advancedcustomfields.com/resources/local-json/) van de velden.

**Fluent Forms Pro**
Voor het maken van de formulieren. Een van de vele formulier plugins op de markt. Deze vinden wij tot nu toe een goede mix hebben tussen features, ondersteuning en gewicht.

**Migrate DB PRO**
Om databases tussen onze omgevingen gesynchroniseerd te houden werken we met Migrate DB PRO om snel databases te pushen/pullen naar andere omgevingen.

**WP Rocket**
Caching laag bovenop WordPress.

**Timber**
Plugin die praat met onze TWIG layer.

## Management van Plugins & WordPress / Composer

Dat doen we met Composer. Elke root folder van een WordPress project heeft een composer.json bestand. Met de command `Composer install` worden alle plugins en WordPress zelf gedownload naar de juiste folders.

## Het thema

Als boilerplate voor ieder project gebruiken wij een minimum thema waar de ondersteuning zit ingebakken voor Twig en een folderstructuur heeft waar we theme partials, components en layouts kunnen plaatsen.

### Timber

Om een MVC model aan te houden in WordPress scheiden we de View laag van de controller laag met de [TWIG template engine](https://twig.symfony.com/). Twig zorgt ervoor dat je view bestanden stukken beter beheersbaar worden. Een voorbeeld:

**Een afbeelding in PHP**:

```php
$thumb_id = get_post_thumbnail_id($post->ID);
$url = wp_get_attachment_url($thumb_id);
<img src="<?php echo $url; ?>" alt="Thumbnail for <?php echo $post->post_title; ?>"  />
```

**Een afbeelding in TWIG**:

```php
<img  src="{{post.thumbnail.src}}"  alt="Thumbnail for {{ post.title }}"  />
```

Timber is de plugin die wij gebruiken om TWIG direct te gebruiken binnen WordPress. Het zorgt ervoor dat WordPress loops en bijvoorbeeld thumbnails zonder enige tussenkomst aangesproken kunnen worden binnen de twig files.
Documentatie over [Timber vind je hier.](https://timber.github.io/docs/)

### SCSS

CSS schrijven we in .scss files die overeen komen met de namen van onze .twig partials. het bestand `partials/footer.twig `heeft dus een scss bestand genaamd `partials/_footer.scss` Het controleren van SCSS op fouten doen we met Prettier en Stylelint.

Documentatie over [SCSS vind je hier](https://sass-lang.com/).

### Javascript

Schrijven we op basis van ES modules met vleugjes jQuery tussendoor :)

### Webpack

Webpack gebruiken we voor het compilen, prefixen, minifien van JS en SCSS en het comprimeren van afbeeldingen/svg's. We hebben een eigen npm module die dit voor ons regelt. Set en forget dus, 9/10 keer.

## Andere tools

- GIT voor versiebeheer
- Github voor het hosten van onze GIT repositories.
- Sourcetree voor visueel versiebeheer
- VScode voor het schrijven van de code
- MAMP/LAMP/XAMMP stack

## Ben jij dit?

Ben jij die flexibele developer die wij zoeken? Ook al kan je misschien niet met alle tools overweg, horen we het graag van je als je de uitdaging ziet zitten. We kunnen je altijd tools uitleggen en je helpen te starten met je eerste project, maar enige basiskennis van moderne webdevelopment is zeer fijn.

Bij vragen, neem gerust contact met ons op.

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->
