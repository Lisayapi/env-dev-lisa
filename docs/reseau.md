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