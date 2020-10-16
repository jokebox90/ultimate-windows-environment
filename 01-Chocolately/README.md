# Chocolately - Gestionnaire de paquets pour Windows

Chocolately est un gestionnaire de paquets pour Windows de la même façon que :

* APT est gestionnaire de paquets pour Debian.
* YUM est gestionnaire de paquets pour CentOS.
* Composer est gestionnaire de paquets pour PHP.
* NPM est gestionnaire de paquets pour NodeJS.

Un gestionnaire de paquet maintient à jour une bibliothèque de logiciels pour un système ou un environnement déterminé. Il met a disposition plusieurs versions des logiciels, gère l'installation des dépendances et la compatibilité entre logiciels, sécurise le téléchargement des logiciels depuis des sources identifiées, etc.

## Prérequis pour l'installation

### Environnement technique utilisé

* **Système :** Windows 10
* **Processeur :** 4 cores
* **Mémoire :** 8GB

### Prise en charge des systèmes Windows

* **Windows 7 / 8 / 10.**

* **Windows 2008(R2) / 2016 / 2019.**

### Prise en charge de PowerShell et .Net Framework

* **PowerShell v3 ou supérieur.**

* **.NET Framework 4.5 ou supérieur.**

## Installation du gestionnaire de paquets

### Accéder à PowerShell

Ouvrir la console PowerShell avec les privilèges Administrateur :

* **Clic-droit sur le Menu Démarrer > Windows PowerShell (Admin).**

### Procéder à l'installation de Chocolately

**Astuce:** Copier-coller les commandes suivantes dans la console PowerShell.

* Activer l'exécution des scripts dans la session PowerShell courante et permet l'installation de Chololately.

```powershell
Set-ExecutionPolicy RemoteSigned -Force
```

* Initialiser une connexion sécurisée pour récupérer le script d'installation de Chocolately depuis le site du projet.

```powershell
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072
$Http = New-Object System.Net.WebClient
$ChocolatelyInstall = $Http.DownloadString('https://chocolatey.org/install.ps1')
```

* Utiliser le script pour installer Chocolately. Si aucune erreur ne se produit, le système est prêt pour utilise Chocolately.

```powershell
Invoke-Expression $ChocolatelyInstall
```

* Faire connaissance et démarrer avec Chocolately.

```powershell
choco -?

# - Quitter pour recharger la console.
exit
```

**Important:** La commannde "choco -?" permet d'afficher un guide détaillé des pratiques et des bonnes pratiques d'administration du gestionnaire de paquets Cholately.

## Installer des outils pour PowerShell et Windows

```powershell
choco install -y powershell-core
choco install -y mls-software-openssh
choco install -y git

# - Quitter pour recharger la console.
exit
```

## Installer des logiciels pour Windows

Une fois PowerShell Core correctement installé :

* **Menu Démarrer > PowerShell > PowerShell 7 > Clic-droit > Plus > Exécuter en tant qu'administrateur.**

### Editer des fichiers avec Visual Studio Code

```powershell
choco install -y vscode
choco install -y vscode-drawio
choco install -y vscode-icons
choco install -y vscode-gitlens
choco install -y vscode-markdownlint
choco install -y vscode-beautify
choco install -y vscode-code-runner
choco install -y vscode-intellicode
choco install -y chocolatey-vscode

# - Quitter pour recharger la console.
exit
```

### Utiliser Linux directement depuis Windows

**Important:** Uniquement pour Windows 10 et Windows Server 2016 / 2019

```powershell
choco install -y wsl2

# - Quitter pour recharger la console.
exit
```

### Utliser des services Docker sur Windows

**Important:** Uniquement pour Windows 10 et Windows Server 2016 / 2019 :

```powershell
choco install -y docker-desktop

# - Quitter pour recharger la console.
exit
```

### Développer et administrer des services Docker

```powershell
choco install -y docker-compose vscode-docker

# - Quitter pour recharger la console.
exit
```

### Améliorer l'ergonomie de la console PowerShell

* Personnaliser l'affichage et les couleurs de la console.

```powershell
choco install -y microsoft-windows-terminal
choco install -y cascadiamonopl
choco install -y cascadiacodepl
Install-Module posh-git -Scope CurrentUser -Force -SkipPublisherCheck
Install-Module oh-my-posh -Scope CurrentUser -Force -SkipPublisherCheck
Install-Module PSReadLine -Scope CurrentUser -Force -SkipPublisherCheck

# - Quitter pour recharger la console.
exit
```

* Personnaliser l'affichage et les couleurs de la console.

```powershell
choco install -y poshhosts

# - Quitter pour recharger la console.
exit
```
