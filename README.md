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

# Sur l'onglet Summary d'une analyse de code, SonarCloud fournit 4 indicateurs. Quels sont-ils et quelles sont leurs utilités ?
- Security : signale les failles potentielles (injections SQL, XSS, accès non autorisés)
- Reliability : signale les erreurs critiques dans le code
- Maintainability : signale les bouts de code difficile à modifier / comprendre...
- Duplications : signale du code dupliqué, copié/collé

# À quoi sert l'indicateur Quality Gate ?
C'est un set de mesures qui indique si le projet est prêt à être déployé en production ou non
en fonction du nombre de mesures acceptables.

# Quelle est la différence entre les sections New code et Overall Code dans l'onglet Summary ?
- New code montre l'analyse seulement sur les changements effectués depuis la dernière analyse
- Overall code montre l'analyse du projet entier

# Y a-t-il des Code Smells ? Si oui, combien et pour quelle(s) raisons(s) ?
Oui il y en a 3, deux car des paramètres dans une fonction sont définis mais non utilisés
et une car deux fonctions avec un nom différent font exactement la même chose

# Y a-t-il des Security Hotspots ? Si oui, combien et pour quelle(s) raison(s) ?
Oui il y en a une car le container dans le Dockerfile est exécuté avec le super user root
ce qui peut poser des problèmes de sécurités

