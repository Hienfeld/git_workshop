
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

### Git Hulp

Als je hulp nodig hebt met Git-commando's:

```sh
git command -help
```

## Git Staging Environment

### Git Staging Environment

Een van de kernfuncties van Git is het concept van de Staging Environment en de Commit.

Terwijl je werkt, kun je bestanden toevoegen, bewerken en verwijderen. Maar telkens wanneer je een mijlpaal bereikt of een deel van het werk voltooit, moet je de bestanden toevoegen aan een Staging Environment.

Gestage bestanden zijn bestanden die klaar zijn om te worden gecommit naar de repository waaraan je werkt. Je leert straks meer over commit.

Voor nu zijn we klaar met werken aan index.html. Dus we kunnen het toevoegen aan de Staging Environment:

### Voorbeeld

```sh
git add index.html
```

Het bestand zou nu gestaged moeten zijn. Laten we de status controleren:

### Voorbeeld

```sh
git status
```

```
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached ..." to unstage)
    new file: index.html
```

Nu is het bestand toegevoegd aan de Staging Environment.

### Meer dan één bestand toevoegen

Je kunt ook meer dan één bestand tegelijk stagen. Laten we nog 2 bestanden toevoegen aan onze werkmap. Gebruik opnieuw de teksteditor.

Een README.md-bestand dat de repository beschrijft (aanbevolen voor alle repositories):

### Voorbeeld

```
# hello-world
Hello World repository for Git tutorial
This is an example repository for the Git tutorial on https://www.w3schools.com

This repository is built step by step in the tutorial.
```

Een basis externe stijlblad (bluestyle.css):

### Voorbeeld

```css
body {
  background-color: lightblue;
}

h1 {
  color: navy;
  margin-left: 20px;
}
```

En update index.html om het stylesheet op te nemen:

### Voorbeeld

```html
<!DOCTYPE html>
<html>
<head>
<title>Hello World!</title>
<link rel="stylesheet" href="bluestyle.css">
</head>
<body>

<h1>Hello world!</h1>
<p>This is the first file in my new Git Repo.</p>

</body>
</html>
```

Voeg nu alle bestanden in de huidige directory toe aan de Staging Environment:

### Voorbeeld

```sh
git add --all
```

Door `--all` te gebruiken in plaats van individuele bestandsnamen, worden alle wijzigingen (nieuwe, gewijzigde en verwijderde bestanden) gestaged.

### Voorbeeld

```sh
git status
```

```
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached ..." to unstage)
        new file:   README.md
        new file:   bluestyle.css
        new file:   index.html
```

Nu zijn alle 3 bestanden toegevoegd aan de Staging Environment en we zijn klaar om onze eerste commit te doen.

Opmerking: De verkorte opdracht voor `git add --all` is `git add -A`

Nu checken we de status van de repository. Maar dit keer gebruiken we de --short optie om de changes compact weer te geven:

```sh
git status --short
```

```
M index.html
```

Note: Short status flags are:

?? - Untracked files
A - Files added to stage
M - Modified files
D - Deleted files
We see the file we expected is modified. So let's commit it directly:

Een laatste shotcut die we laten zien is om direct een commit te doen, zonder eerst te stages. Dit is niet gebruikelijk, maar kan wel.

```sh
git commit -a -m "Updated index.html with a new line"
```
```
[master 09f4acd] Updated index.html with a new line
 1 file changed, 1 insertion(+)
 ```