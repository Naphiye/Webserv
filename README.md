un **serveur HTTP** en **C++98**, respectant la norme **RFC 7230**.  
L’objectif est de comprendre en profondeur le fonctionnement du protocole HTTP et des serveurs web.  

## Objectifs

- Implémenter un serveur HTTP capable de gérer :  
  - Les méthodes **GET**, **POST**, **DELETE**  
  - Le parsing et la validation des requêtes HTTP  
  - La gestion de plusieurs **virtual hosts** et **routes**  
- Gérer les **erreurs HTTP** (pages personnalisées)  
- Supporter l’**upload de fichiers**, le **CGI** et les limites de body  

## Structure du projet

- `src/` : code source du serveur (parsing, socket, HTTP handling)  
- `www/server_config.txt` : fichier de configuration (format type NGINX)  
- `Makefile` : compilation du projet  

## Lancement

```bash
make
./webserv www/server_config.txt
