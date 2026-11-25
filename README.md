# env-dev-lisa - (B1 DEV, IFRAN)

Environnement de Lisa - B1 DEV,IFRAN


## Mon ordinateur 
 
| Élément     | Valeur                                                | 
| ----------- | ----------------------------------------------------- | 
| Système     | Windows 11 Famille                                    | 
| Processeur  | ntel(R) Core(TM) i5-8350U CPU @ 1.70GHz (1.90 GHz)    | 
| Mémoire     | 16,0 Go                                               | 
| Éditeur     | VS Code                                               | 
 
## Mon Ubuntu 
 
| Élément      | Valeur               | 
| ------------ | -------------------- | 
| Version      | Ubuntu 24.04.4 LTS   | 
| Lancé avec   | WSL                  | 
| Processeurs  | 8                    | 
| Mémoire      | 7,7 Go               | 
| Utilisateur  | lisa                 |

## Logiciels installés dans Ubuntu 
| Logiciel | Version  | Commande d'installation                              | 
| -------- | -------- | ---------------------------------------------------- | 
| Git      | 2.43.0   | déjà présent dans Ubuntu                             | 
| tree     | 2.1.1    | `sudo apt install -y tree`                           | 
| htop     | 3.3.0    | `sudo apt install -y htop`                           | 
| nano     | 7.2      | `sudo apt install -y nano`                           | 
| Node.js  | 26.xx    | dépôt NodeSource, puis `sudo apt install -y nodejs`  | 
| npm     | 11.xx     | installé avec Node.js                                |  

## Historique 
 
Ce dossier est suivi avec Git depuis le sous-module 2

## Installation

### 1. Installer Ubuntu et VS Code

- **Windows :** dans le Terminal (administrateur), taper `wsl --install`, redémarrer, puis choisir un nom d'utilisateur et un mot de passe Ubuntu.
- **Mac :** installer Homebrew depuis [brew.sh](https://brew.sh), puis taper `brew install colima docker`, `colima start` et `colima ssh`.
- Installer VS Code depuis [code.visualstudio.com](https://code.visualstudio.com).

### 2. Installer les outils dans Ubuntu

1. Ouvrir Ubuntu et aller dans le dossier du projet : `cd ~/dev/env-dev-kone`
2. Lancer le script d'installation : `./scripts/installer.sh`

## Vérification

Lancer `./scripts/verifier.sh` dans Ubuntu.

Résultat attendu : une version pour Ubuntu, Git, Node.js, npm, tree et Python, puis `HTTP/2 200` pour l'accès à GitHub.

## Contenu du dossier

| Fichier ou dossier     | Rôle                                                         |
| ---------------------- | ------------------------------------------------------------ |
| `README.md`            | Cette documentation                                          |
| `JOURNAL.md`           | Le journal de mes choix                                      |
| `docs/reseau.md`       | Ma fiche de réseau                                           |
| `docs/aide-memoire.md` | Mon aide-mémoire des commandes du terminal Linux             |
| `scripts/installer.sh` | Script qui installe les outils (Git, Node.js, npm, tree…)    |
| `scripts/verifier.sh`  | Script qui affiche les versions pour vérifier l'installation |
