
# SSH Configureren op Windows

Deze handleiding beschrijft hoe je SSH kunt configureren op Windows om verbinding te maken met GitHub.

## Stap 1: Genereer een SSH-sleutel

1. **Open Git Bash**
   - Als je Git voor Windows nog niet hebt geïnstalleerd, download en installeer het van [git-scm.com](https://git-scm.com/).

2. **Genereer een nieuwe SSH-sleutel**
   - Open Git Bash en voer het volgende commando uit. Vervang `your_email@example.com` door je GitHub-e-mailadres:

```sh
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

   - Je wordt gevraagd om een bestand op te geven waarin de sleutel moet worden opgeslagen. Druk op Enter om de standaard bestandslocatie te accepteren.
   - Voer een wachtwoordzin in wanneer daarom wordt gevraagd voor extra beveiliging (optioneel).

## Stap 2: Start de SSH-agent

1. **Start de SSH-agent**
   - Voer de volgende commando's uit in Git Bash om de SSH-agent te starten:

```sh
eval "$(ssh-agent -s)"
```

   - Je zou output moeten zien zoals `Agent pid 59566`.

2. **Voeg je SSH-sleutel toe aan de SSH-agent**

```sh
ssh-add ~/.ssh/id_rsa
```

## Stap 3: Voeg de SSH-sleutel toe aan je GitHub-account

1. **Kopieer de SSH-sleutel naar je klembord**
   - Voer het volgende commando uit om de SSH-sleutel naar je klembord te kopiëren:

```sh
clip < ~/.ssh/id_rsa.pub
```

2. **Voeg de sleutel toe aan GitHub**
   - Ga naar GitHub en log in op je account.
   - Klik in de rechterbovenhoek van een pagina op je profielfoto en vervolgens op `Settings`.
   - Klik in de zijbalk met gebruikersinstellingen op `SSH and GPG keys`.
   - Klik op `New SSH key` of `Add SSH key`.
   - Voeg een beschrijvende titel toe voor de nieuwe sleutel in het veld "Title".
   - Plak je sleutel in het veld "Key".
   - Klik op `Add SSH key`.
   - Bevestig je GitHub-wachtwoord.

## Stap 4: Configureer Git om SSH te gebruiken

1. **Wijzig de URL van de externe repository om SSH te gebruiken**
   - Navigeer naar je projectdirectory en stel de externe URL in om SSH te gebruiken:

```sh
git remote set-url origin git@github.com:your_github_username/your_repository.git
```

Vervang `your_github_username` en `your_repository` door je daadwerkelijke GitHub-gebruikersnaam en de naam van je repository.

## Stap 5: Test de SSH-verbinding

1. **Test de SSH-verbinding**

```sh
ssh -T git@github.com
```

   - Je zou een bericht moeten zien zoals:

```
Hi your_github_username! You've successfully authenticated, but GitHub does not provide shell access.
```

## Voorbeeld

Hier is een voorbeeld dat alle stappen samenvat:

1. **Genereer SSH-sleutel**

```sh
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

2. **Start SSH-agent en voeg sleutel toe**

```sh
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```

3. **Kopieer SSH-sleutel naar klembord**

```sh
clip < ~/.ssh/id_rsa.pub
```

4. **Voeg SSH-sleutel toe aan GitHub**
   - Ga naar GitHub `Settings` > `SSH and GPG keys` > `New SSH key`
   - Plak de sleutel en sla deze op.

5. **Configureer Git om SSH te gebruiken**

```sh
git remote set-url origin git@github.com:your_github_username/your_repository.git
```

6. **Test SSH-verbinding**

```sh
ssh -T git@github.com
```

Nu zou je SSH-configuratie op Windows compleet moeten zijn en kun je met SSH naar je GitHub-repositories pushen.
