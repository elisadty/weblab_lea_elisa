# Projet web programming

## Construction d'un site de système de gestion de bibliothèque

Afin d'acceder au site/ lancer le projet, il faut run le code dans deux terminaux en même temps :
le 1er pour lancer uvicorn :

```bash
(venv) PS C:\Users\Elisa\OneDrive\Documents\EPF\webgit> uvicorn src.main:app --reload
```bash

et le 2ème pour accéder au site :

```bash
(venv) PS C:\Users\Elisa\OneDrive\Documents\EPF\webgit\frontend> python .\server.py
```bash

-> ouvrez ensuite votre navigateur à l'adresse :
```bash http://localhost:5000 ```bash

Pour voir les bug dans le devtools (sur le site), il est possible de faire un f12.


-------------------------------------------------------------------------------------------------
Pour lancer les units test :
pytest tests/services/ -v

Pour tester un par un :
pytest tests/services/test_books.py -v
pytest tests/services/test_users.py -v
pytest tests/services/test_loans.py -v
