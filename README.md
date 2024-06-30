
# Git Workshop voor Collega's

Welkom bij de Git Workshop! Deze tutorial is ontworpen om je te helpen Git te begrijpen en te gebruiken door middel van praktische voorbeelden. Laten we beginnen!

## Leren door Voorbeelden

In deze tutorial laten we Git-commando's zien zoals deze:

### Voorbeeld

```sh
git --version
```

Uitvoer:
```
git version 2.30.2.windows.1
```

Voor nieuwe gebruikers kan het terminalvenster een beetje ingewikkeld lijken. Maak je geen zorgen! We houden het echt simpel, en op deze manier leren geeft je een goed begrip van hoe Git werkt.

In de bovenstaande code kun je commando's (invoer) en uitvoer zien.

### Invoer Commando:

```sh
git --version
```

### Uitvoer:

```
git version 2.30.2.windows.1
```

In het algemeen zijn regels met `$` ervoor invoercommando's. Dit zijn de commando's die je kunt kopiëren en uitvoeren in je terminal.

## Platform Wijzigen:

Schakel focus naar:
- GitHub
- Bitbucket
- GitLab

## Git en Externe Repositories

Git en GitHub zijn verschillende dingen. In deze tutorial leggen we uit wat Git is en hoe je het kunt gebruiken op externe repositoryplatforms zoals GitHub.

Je kunt kiezen en veranderen op welk platform je je wilt richten door in het menu aan de rechterkant te klikken: GitHub, GitLab, Bitbucket.

## Git en GitHub Introductie

### Wat is Git?

Git is een populair versiebeheersysteem gemaakt door Linus Torvalds in 2005, onderhouden door Junio Hamano.

**Gebruik:**
- Bijhouden van codewijzigingen
- Bijhouden wie wijzigingen heeft aangebracht
- Samenwerking bij codering

### Wat doet Git?

- Beheer projecten met Repositories
- Clone een project om aan een lokale kopie te werken
- Controleer en volg wijzigingen met Staging en Committing
- Branch en Merge om aan verschillende delen en versies van een project te werken
- Haal de laatste versie van het project naar een lokale kopie
- Push lokale updates naar het hoofdproject

## Werken met Git

- Initialiseer Git op een map, waardoor het een Repository wordt
- Git maakt een verborgen map aan om wijzigingen in die map bij te houden
- Wanneer een bestand wordt gewijzigd, toegevoegd of verwijderd, wordt het als gewijzigd beschouwd
- Selecteer de gewijzigde bestanden die je wilt Stagen
- De Gestagede bestanden worden Gecommit, waarbij Git een permanente momentopname van de bestanden opslaat
- Git stelt je in staat om de volledige geschiedenis van elke commit te zien
- Je kunt terugkeren naar elke eerdere commit
- Git slaat geen aparte kopie van elk bestand in elke commit op, maar houdt bij welke wijzigingen in elke commit zijn aangebracht

## Waarom Git?

- Meer dan 70% van de ontwikkelaars gebruikt Git!
- Ontwikkelaars kunnen overal ter wereld samenwerken.
- Ontwikkelaars kunnen de volledige geschiedenis van het project zien.
- Ontwikkelaars kunnen terugkeren naar eerdere versies van een project.

## Wat is GitHub?

GitHub maakt tools die Git gebruiken. Het is de grootste host van broncode ter wereld en is sinds 2018 eigendom van Microsoft.

In deze tutorial zullen we ons richten op het gebruik van Git met GitHub.

## Git Aan de Slag

### Git Installeren

Je kunt Git gratis downloaden van de volgende website: [Git SCM](https://www.git-scm.com/)

### Git gebruiken met Command Line

Om Git te gaan gebruiken, open je je Command shell.

- Voor Windows kun je Git Bash gebruiken, inbegrepen in Git voor Windows.
- Voor Mac en Linux gebruik je de ingebouwde terminal.

Controleer of Git correct is geïnstalleerd:

```sh
git --version
```

### Git Configureren

Stel je gebruikersnaam en e-mail in:

```sh
git config --global user.name "your-username"
git config --global user.email "your-email"
```

### Git Map Maken

Maak een nieuwe map voor je project:

```sh
mkdir myproject
cd myproject
```

Initialiseer Git in de map:

```sh
git init
```

### Nieuwe Bestanden Toevoegen

Maak en sla een HTML-bestand op met de naam `index.html` in de map.

```html
<!DOCTYPE html>
    <html>
    <head>
        <title>Hello World!</title>
    </head>
    <body>

        <h1>Hello world!</h1>
        <p>This is the first file in my new Git Repo.</p>

    </body>
</html>
```

Controleer de status:

```sh
git status
```

Stage het bestand:

```sh
git add index.html
```

Commit het bestand:

```sh
git commit -m "First release of Hello World!"
```

### Git Hulp

Als je hulp nodig hebt met Git-commando's:

```sh
git command -help
```

## Werken met Git Branches

Maak een nieuwe branch:

```sh
git branch hello-world-images
```

Schakel over naar de nieuwe branch:

```sh
git checkout hello-world-images
```

Voeg wijzigingen toe en commit deze naar de branch:

```sh
git add --all
git commit -m "Added image to Hello World"
```

### Branches Samenvoegen

Schakel terug naar master en voeg branches samen:

```sh
git checkout master
git merge hello-world-images
```

Los eventuele merge-conflicten op en commit de wijzigingen:

```sh
git commit -m "merged with hello-world-images after fixing conflicts"
```

Verwijder de samengevoegde branch:

```sh
git branch -d hello-world-images
```

Nu je een beter begrip hebt van hoe branches en samenvoegen werken, is het tijd om te beginnen met werken met een externe repository!
