# Webserv 🌐

Ce projet consiste à développer un **serveur HTTP** en **C++98**, respectant la norme **RFC 7230**.  
L’objectif est de comprendre en profondeur le fonctionnement du protocole HTTP et des serveurs web, tout en implémentant un serveur performant, robuste et sécurisé.

Ce projet a été réalisé en **groupe avec [Antoine Jourdan Astruc](https://github.com/Ajap75) et [Jerome Portier](https://github.com/jeportie)**.

---

## 🎯 Objectifs

- Implémenter un serveur HTTP capable de gérer :  
  - Les méthodes **GET**, **POST**, **DELETE**  
  - Le parsing et la validation des requêtes HTTP  
  - La gestion de plusieurs **virtual hosts** et **routes**  
- Gérer les **erreurs HTTP** avec des pages personnalisées  
- Supporter l’**upload de fichiers**, le **CGI** et les limites de body définies dans la configuration  
- Maintenir une architecture claire, modulaire et respectant les normes de l’école 42  
- **Sécuriser le serveur** autant que possible
---

## 🏗️ Structure du projet

- `src/` : code source du serveur (parsing, socket, gestion HTTP, validation)  
- `www/server_config.txt` : fichier de configuration principal (format inspiré de NGINX)  
- `Makefile` : compilation du projet  

---

## 🚀 Lancement

1. Compiler le projet :
 ```bash 
make  
```

2. Lancer le serveur avec le fichier de configuration :
```bash
./webserv www/server_config.txt  
```

3. Le serveur est accessible via votre navigateur ou via `curl` sur le port défini dans la configuration.  

## 💡 Notes

- Chaque virtual host peut avoir ses propres routes, pages d’erreur et limites de body et les méthodes supportées.  
- Le serveur supporte les scripts CGI em php pour exécuter des programmes côté serveur.  
- Une attention particulière a été portée à la validation stricte des requêtes pour éviter les comportements indéfinis ou les crashs.  
- La sécurité a été renforcée pour éviter les buffer overflows dans les headers et autres entrées critiques(details a venir).
