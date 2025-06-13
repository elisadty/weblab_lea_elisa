# Système de gestion de bibliothèque (web programming)
## Présentation 
Ce projet est organisé selon une architecture n-tiers : frontend, buisiness layer (backend), data layer.
Cette architecture permet de séparer clairement des responsabilités ce qui est plus facile pour debugger en cas de problème, contrairement à un unique bloc de code.

### Frontend (Présentation)
- Technologies : HTML, CSS, JavaScript
- Rôle : Interface utilisateur, gestion de l’interaction avec l’utilisateur (connexion, affichage des livres, profil, etc.)
- Dossier : /frontend
Il fonctionne comme une application SPA (Single Page Application) qui communique avec le backend via des API.

### Backend (Logique métier et API)
- Technologies : Python avec FastAPI (ou autre framework selon ton cas)
- Rôle : Gère la logique métier, la validation des données, l’authentification, et expose des API RESTful pour le frontend.
- Dossier : /src 

Il traite les requêtes du frontend et interagit avec la couche de données.

### Database layer
- Type : Base relationnelle (SQLAlchemy)
- Rôle : Stockage persistant des données (utilisateurs, livres, prêts, etc.)

La communication avec la base se fait via un ORM ou des requêtes SQL dans le backend.

-------------------------------------------------------------------------------------------------

### Lancer le projet
Afin d'acceder au site/ lancer le projet, il faut run le code dans deux terminaux en même temps :
le 1er pour lancer uvicorn :
```bash
(venv) PS C:\Users\Elisa\OneDrive\Documents\EPF\webgit\frontend> python .\server.py
````
et le 2ème pour accéder au site :

```bash
(venv) PS C:\Users\Elisa\OneDrive\Documents\EPF\webgit\frontend> python .\server.py
```

-> ouvrez ensuite votre navigateur à l'adresse :
```bash 
http://localhost:5000
```

Pour voir les bug dans le devtools (sur le site), il est possible de faire un f12.


-------------------------------------------------------------------------------------------------
Pour lancer les units test :
``` bash
pytest tests/services/ -v
```

Pour tester un par un :
```bash
pytest tests/services/test_books.py -v
pytest tests/services/test_users.py -v
pytest tests/services/test_loans.py -v
```

### Les fonctionnalités ajoutées
- modification du mdp + reconnexion avec
- compte admin


Léa et Élisa
