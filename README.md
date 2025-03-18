# TP2

# Quelles étapes (steps) sont réalisées par cette action ?
- Checkout du code
    - Télécharge le code source du repository.

- Installation de Python 3.10

- Installation des dépendances
    - Met à jour pip et installe les dépendances (flake8, pytest) et les paquets dans requirements.txt si ça existe.

- Linting avec flake8
    - Vérifie le code source pour détecter les erreurs de syntaxe et les noms non définis.

- Exécution des tests avec pytest

# Une étape est définie au minimum par 2 éléments, lesquels sont-ils et à quoi servent-ils ?
- name : le nom de l'étape affiché dans les logs.
- run ou uses :
    - run: permet d'exécuter des commandes shell.
    - uses: permet d'utiliser une action GitHub déjà existante.

# La première étape contient le mot-clé 'with', a quoi sert-il ?
With est utilisé pour passer des arguments à l'action GitHub définie dans uses.
Là on lui donne la version de python précise à installer.