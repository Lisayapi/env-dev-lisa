# Fiche réseau 
 
## Mes adresses IP 
 
| Machine                | Adresse IP      | Privée ou publique ? | 
| ---------------------- | --------------  | -------------------- | 
| Mon Ubuntu             | 192.168.108.144 | Privé                | 
| Mon ordinateur (Wi-Fi) | 192.168.108.144 | Privé                | 
| Ma connexion Internet  | (non publiée)   | publique             | 
 
## Résultats du DNS 
 
| Nom de domaine  | Adresse IP           | 
| --------------- | -------------------- | 
| `github.com`    | 140.82.121.3         | 
| `wikipedia.org` | 185.15.59.224        | 
 
## Les outils réseau 
 
| Commande             | Ce qu'elle fait                                                            | 
| -------------------- | -------------------------------------------------------------------------- | 
| `hostname -I`        | Affiche l'adresse IP de mon Ubuntu                                         | 
| `ping -c 4 <nom>`    | Envoie 4 paquets à la machine indiqué pour vérifié si elle est joingnable  | 
| `nslookup <nom>`     | Recherche l'adress IP associée au nom de domaine indiqué                   |

## Le trajet d'une requête 
 
Quand je tape `https://github.com` dans mon navigateur : 
 
1. … 
2. … 
3. … 
4. … 
5. … 
6. … 
 
## Les codes de réponse HTTP 
 
| Code | Nom                   | Ce qu'il veut dire | Exemple que j'ai vu | 
| ---- | --------------------- | ------------------ | ------------------- | 
| 200  | OK                    | …                  | …                   | 
| 301  | Moved Permanently     | …                  | …                   | 
| 404  | Not Found             | …                  | …                   | 
| 500  | Internal Server Error | …                  | (pas vu)            | 

## Les ports

| Port | Service | Exemple d'URL |
| ---- | ------- | ------------- |
| 80   | HTTP (web non chiffré) | http://example.com |
| 443  | HTTPS (web chiffré, avec le cadenas) | https://example.com |
| 8000 | Serveur de développement local (notre site) | http://localhost:8000 |

## Diagnostiquer une erreur

Les 4 questions, dans l'ordre :

1. Le nom est-il trouvé ? → `nslookup <nom>`
2. Le port est-il ouvert (le serveur écoute-t-il) ? → `ss -tln` / `curl -I http://<nom>:<port>`
3. Que répond le serveur (quel code HTTP) ? → `curl -I <url>` ou le journal du serveur (200, 404…)
4. Le fichier demandé existe-t-il au bon endroit, avec le bon nom ? → `ls`

### Exemple 2 : le logo n'apparaît pas
 - **Symptôme :** une icône d'image cassée s'affiche à la place du logo
 - **Étape :** question 4, le serveur cherche le fichier
 - **Cause :** le navigateur demande `/images/logo.svg`, mais `logo.svg` est à la racine du site et le dossier `images` n'existe pas (journal : `GET /images/logo.svg ... 404`)
 - **Correction :** `mkdir images` puis `mv logo.svg images/`
 - **Vérification :** le logo s'affiche, et le journal montre `GET /images/logo.svg ... 200`
